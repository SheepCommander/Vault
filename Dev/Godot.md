### Music
https://youtu.be/q2dfKFhcIGg


### Object Pooling
[5 Code Patterns](https://youtu.be/UuEqUN98uZo?t=229) (Async Callbacks, Signal Bus, Object Pooling, composition?, Data)
[5 Code Patterns](https://youtu.be/oIrvZDDWxhU) (inheritance, DataClass, feature tags, *fluent interface*,  FSM)
```gdscript
const scene = preload("res://scenes/icon.tscn")

func _physics_process(delta: float) -> void:
	for i in 750:
		var instance = ObjectPool.instantiate(sceneToInstantiate)
		add_child(instance)
		ObjectPool.returnInstance(instance, sceneToInstantiate)
```

```gdscript
extends Node # Autoload ObjectPool

var instances : Dictionary #PackedScene -> array[scene instances]

func instantiate(scene: PackedScene):
	var existingInstances = instances.get(scene, null)

	if existingInstances:
		var instance = existingInstances.pop_back()
		if existingInstances.is_empty():
			instances.erase(scene)
		instance.request_ready()
		if "poolingHandle" in instance:
			instance.poolingHandle = scene
		return instance

	else:
		var instance = scene.instantiate()
		instance.prepare()
		if "poolingHandle" in instance:
			instance.poolingHandle = scene
		return instance
```

```gdscript
extends Sprite2D

var animation

func prepare() -> void:
	animation = $AnimationPlayer
```