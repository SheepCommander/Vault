@export var node_path: NodePath = ^"button"

mob.died.connect(func():
	spawnh()
	increaseh()
)

https://youtu.be/siK7mjyW2Rg?list=PLIPN1rqO-3eHRuQI_zNbHMGB7Tj8UvM7p
2. Switch rgb to RAW mode to go above 1. Allows glow, translucency, etc.
3. global_position and global_rotation
4. Enums can be accessed anywhere with class_name, and they work like normal dicts with .keys and .values
5. Curve textures: pass to Material/Shader/ShaderParam
7. Viewport- everything w/in is drawn on an extra canvas. Pass it to a Texture or Shader or...
9. Matrix.IDENTITY Transform.IDENTITY Color.Transparent Color.white Color.black - esp w/ t weens
10. set_process(false)  hide()   remove_child()   queue_free()    get_tree().paused = true    VisualServer.set_shader_time_scale(0)
11. @tool
---
1. Particle emission masks (.png)
3. enter_tree & ready: Super called first.  process & exit_tree: Subclass called first.
	- call super with . in front of call
4. Particle shaders = how it moves & fragment() how an object looks
6. root.find_node()
7. Curves help polish everything. curve textures can also be passed to a shader.
8. Two objects collide when one has a Mask that overlaps w/ another's Layer.
---
1. Ctrl + Shift + E *evaluate expressions!!*
2. Use canvasitem material to chose Blend mode. Mix or Add? Use Mix, turn on Raw, set modulate higher than one & use transparency
4. SpriteRegion wrapping! Wrapping textures!!
6. `func _draw(): draw_circle()`
8. Object.set_meta("creation_time", OS.get_time())   .has_meta()   .get_meta()
9. **yield(get_tree(), "idle_frame")**  ?
10. Turn on Show Ruler, click and drag to create reference line in 2d
---
