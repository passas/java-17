```Java
String query = "SELECT * FROM music.artists";

try ( var connection = ... ;
      Statement statement = connection.createStatement();
)
{
  ResultSet resultSet = statement.executeQuery(query);
  var meta = resultSet.getMetaData();
  while (resultSet.next())
    System.out.printf("%d %s %n", resultSet.getInt(1), resultSet.getString("artist_name"));    // column index || column label   
} 
```
