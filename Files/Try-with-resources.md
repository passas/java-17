```Java
String fileName = "file.csv";
```

```Java
Path path = Paths.get(filename);
FileReader fileReader = null;
try
{
  fileReader = new FileReader(filename);
}
catch (IOException e)
{
  ...
}
finally
{
  if (fileReader != null)
    try
    {
      fileReader.close();
    }
    catch(IOException e)
    { ... }
}
```

jdk-17 (try-with-resources)
```Java
Path path = Paths.get(filename);
FileReader fileReader = null;
try(fileReader = new FileReader(filename))
{
}
catch (FileNotFoundException e) // open
{
  ...
}
catch (NullPointerException | IllegalArgumentException badData)
{
  ...
}
catch (IOException e) // read ; close
{
  ...
}
catch (Exception e)
{
  ...
}
```
