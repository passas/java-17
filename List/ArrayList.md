Aggregation

Dynamic

Unordered

Same object can appear more than once

```Java
ArrayList<Object> arrayList = new ArrayList<>();

arrayList.add(new Object());
```

```Java
for (int i=0; i<arrayList.size(); i++) o;

for (Object o : arrayList) o;

arrayList.forEach();

arrayList.stream();
```

---

```Java
Object[] array = {new Object(), new Object};

ArrayList<Object> arrayList = new ArrayList<>(List.of(array));
```
