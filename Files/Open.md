```Java
String fileName = "file.csv";
```

```Java
Path path = Paths.get(filename);
try
{
  List<String> lines = Files.readAllLines(path);
}
catch (IOException e)
{
  ...
}
```

```Java
File file = new File(filename);
if (!file.exists()) ...
```
