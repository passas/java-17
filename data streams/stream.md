```Java
var stream = .stream()

var map = .stream().map()

var filter = .stream().map().filter()

var filter = map.filter()

var filter_2nd = map.filter() // error
```

```Java
.boxed().map() <=> .mapToObj()
```

```Java
.toList()

.toArray(MyObject::new)

.collect(Collectors.toList());

.collect(Collectors.toCollection(ArrayList::new));

.collect(Collectors.groupingBy(MyClass::getField));
```
