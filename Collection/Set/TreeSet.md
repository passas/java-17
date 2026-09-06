TreeSet < NavigableSet < SortedSet < Set < Collection

Need to implement Comparable or provide a Comparator on instance

```Java
Comparator<Contact> sort = Comparator.comparing(Contact::getName);
NavigableSet<Contact> set = new TreeSet<>(sort);
set.addAll(list);

set.comparator();
```

```Java
Collections.min(set, set.comparator()); // peak

set.first(); // peak

set.pollFirst(); // remove
```

```Java
.headSet(new Object(), true | false);
.tailSet(new Object(), true | false);
.subSet( );
```
