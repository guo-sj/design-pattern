### 备忘录模式(Memento Pattern)

> 在不破坏封装的前提下，捕获一个对象的内部状态，并在该对象之外保存该状态，这样可以在以后对对象恢复到原先保存的状态。
它是一种对象行为型模式，其别名是 Token。

类图如下：

```mermaid
---
title: Memento Pattern
---
classDiagram
    direction LR
    Memento <.. Originator
    Caretaker o-- Memento : memento
    class Originator{
        -state
        +restoreMemento(Memento m)
        +createMemento()
    }
    class Memento{
        -state
        +getState()
        +setState()
    }
    class Caretaker{
        -Memento memento
    }
```
