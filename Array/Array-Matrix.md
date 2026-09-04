```Java
int[][] matrix = new int[2][2];
```

```Java
int[][] matrix = {
                    {0,1},
                    {1,2}
                };
```

```Java
int[2][] matrix;
for(int i =0; i<matrix.length; i++) matrix[i] = new int[2];
```

```Java
for(int i=0; i<matrix.length; i++)
  for(int j=0; j<matrix[i].length; j++)
    matrix[i][j];

for(var outter : matrix)
  for (var elem : outter)
    elem;
```

---

```Java
int[] arr = new int[2];
int[][] arr = new int[2][2];
int[][][] arr = new int[2][2][2];

Array.deppToString(arr);
```
