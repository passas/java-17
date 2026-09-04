```Java
ArrayList<Object> arrayList = new ArrayList<>();

Object[] array = arrayList.toArray(new Object[arrayList.size()]);
```

---

Mutable
```Java
Object[] array = {new Object(), new Object()};
    ArrayList<Object> arrayList = Arrays.stream(array).collect(Collectors.toCollection(ArrayList::new));

int[] array = {1, 2};
ArrayList<Integer> arrayList = Arrays.stream(array).boxed().collect(Collectors.toCollection(ArrayList::new));
```

Mutable, not resizable

```Java
Object[] array = {new Object(), new Object};

ArrayList<Object> arrayList = Array.asList(array);
```

Immutable 

```Java
Object[] array = {new Object(), new Object};

ArrayList<Object> arrayList = new ArrayList<>(List.of(array));
```
