```Java
try( BufferedReader bufferedReader = new BufferedReader( new FileReader ( "file.csv" ) ) )
{
  String line;
  while ( (line = bufferedReader.readLine() != null) )
  {
    ...
  }
}
catch (IOException e)
{
  ...
}
```

```Java
bufferedReader.lines().forEach();
```
