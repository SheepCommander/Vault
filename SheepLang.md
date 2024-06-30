I want a language that is procedural, statically typed, and has Optional/Union types, defer keyword, comptime, and structs.

I want the best parts of GDScript, Zig, there are no good parts in Java, and I'm not sure what else.

I want the language to be closer to GDScript in indents and simplicity, but still somewhat more towards Zig.

```sheeplang
## SceneLoader loads a target scene asyncrously in the background.
extends Node

# -- Public vars
## The scene that's currently being switched to.
static var current_target: PackedScene = null

## The scene you want to load & switch to. Use [method switch_scene].
## Note: Use a [ResourcePreloader] if more resources need to be loaded.
@export var target_scene: PackedScene

## The loading screen you want to display while loading.
@export var loading_screens: Array[PackedScene]

## Starts async loading on _ready(). Else, load on [method switch_scene]
## or [method start_loading_scene].
@export var start_load_on_ready := true

## Main threads will load faster, but may slow down the game.
## Once loading, this option cannot be changed.
@export var use_main_threads := false

# -- Private vars
@onready var RL := ResourceLoader


func _ready():
	if not target_scene:
		printerr("Load target empty! - ", get_tree().root.get_path_to(self))
		queue_free()
		return
	
	if loading_screens.is_empty():
		printerr("No loading screen! - ", get_tree().root.get_path_to(self))
		queue_free()
		return
	
	if start_load_on_ready:
		start_loading_scene()


## Starts loading the [member target_scene] in the background.
func start_loading_scene() -> void:
	RL.load_threaded_request(target_scene.resource_path,"",accelerated_loading)

## Immediately attempt to switch scene, putting up the loading screen.
## [param remove_prev_scene] will remove the Main scene.
## Does not work if already trying to switch to a different scene.
func switch_scene(remove_prev_scene := false) -> void:
	if current_target != null:
		printerr("Can't scene switch! - ", get_tree().root.get_path_to(self))
		return
	start_loading_scene()
	var target := RL.load_threaded_get(target_scene.resource_path)
	
```