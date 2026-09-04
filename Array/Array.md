```Java
int[] array = new int[2]
```

```Java
int[] array = new int[]{0,1}

int[] array = {0,1}
```

```Java
for(int i=0; i < array.length; i++) array[i];

for(int elm : array) elm;

Arrays.stream(array).forEach(System.out::println);
Arrays.stream(array).forEach((i -> System.out.println(i)));
```
