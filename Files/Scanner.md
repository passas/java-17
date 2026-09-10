```Java
try( Scanner scanner = new Scanner ( new File("file.csv") ) )
{
  while(scnaner.hasNextLine())
    ...
}
catch ( FileNotFoundException e )
{}
```

```Java
scanner.delimeter();
scanner.useDelimeter("$");
scanner.tokens().forEach();
```
