### What is `_` ???
`_` is kind of a "default" or "ignore" keyword of sorts.
Zig requires you to use all variables. You can assign `_ = my_var;` in order to ignore it.

Most useful for `_ = addNode();` when u dont care abt a method's return.

Also used for `const array = [_]u8{'h', 'i'}` to infer length of array.

### How do I print???
```zig
std.debug.print("Character: {c}, String: {s}, Number: {d}\n", .{'a',"Pp", 5});
```

### What is `.{1, 2, 5}`??
If you create an Array with `.{}` that is an Anonymous array/tuple/whatevs.

Meaning that you do not store a reference to it, u just create it.

### How do I `.toUpper()`??
Check `std` library docs. `std.ascii.toUpper(c: u8)`

### How do I build and crap??
```cmd
zig run main.zig
zig test main.zig
zig run src/main.zig
```
### What is `usize`?????
[On 64 bit PCs its u64 & 32bit PCs its u32](https://ziggit.dev/t/what-is-usize/3390/3)
