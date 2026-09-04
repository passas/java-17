```Java
ArrayList<Object> arrayList = new ArrayList<>();

Object[] array = arrayList.toArray(new Object[arrayList.size()]);
```

---

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
