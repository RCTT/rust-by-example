变量负责释放它们的资源(如果变量拥有资源)，资源只能有**一个**所有者，否则会被多次释放。

当执行赋值 `let x = y`，或通过值 `foo(x)` 传递函数参数时，资源的**所有权**(如果分配了资源)被转移，这在 rust 中被称为“转移”。

After moving resources, the previous owner can no longer be used. This avoids
the creation of *dangling pointers*.资源（的所有权）转以后，先前的资源所有者不能在使用这些资源。这避免了产生**悬垂指针**。

{move.play}
