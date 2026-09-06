No guarantee order

int hashCode

```Java
Set<Object> union = new HashSet<>(setA);
union.addAll(setB);
```

```Java
Set<Object> intersection = new HashSet<>(setA);
intersection.retainAll(setB);
```

Assymetric:
```Java
Set<Object> minus = new HashSet<>(setA);
minus.removeAll(setB);
```

Outter:
```Java
Set<Object> outter = new HashSet<>(minus);
outter.removeAll(setA);

Set<Object> outter = new HashSet<>(union);
outter.removeAll(intersection);
```
