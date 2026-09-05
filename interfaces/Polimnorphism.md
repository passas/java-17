```Java
MyInterface x = new MyClass();

x.<interface method>

((MyClass) x).<instance method>


if (x instanceof MyClass myClass)    // jdk-17
  myClass.<instance method>          // jdk-17
```

```Java
List<MyInterface> ...
```

