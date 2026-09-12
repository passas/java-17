```Java
Properties properties = new Properties();
try
{
  properties.load(Files.newInputStream(Path.of("sql.properties")), StandardOperation.READ);
}
catch( IOException e )
{}

properties.getProperty("..."); // String
```
