```Java
var dataSource = new MySqlDataSource();

dataSOurce.setServerName("localhost");
dataSOurce.setPort(3306);
dataSOurce.setDatabaseName("music");
dataSOurce.setUser();
dataSOurce.setPassword();
try
{
  dataSource.setContinueBatchOnError(false);
}
catch (SQLException e)
{
  throw new RuntimeException(e);
}

try (Connection connection = dataSource.getConnection(System.getenv("MYSQL_USER"), System.getenv("MYSQL_PASS")))
{
  String sql = "SELECT * FROM music.albumview WHERE artist_name = ?";
  PreparedStatement ps = connection.prepareStatement(sql);
  ps.setString(1, "Elf");
  ResultSet resultSet = ps.executeQuery();
}
catch (SQLException e)
{
  e.printStackTrace();
}
```

```Java
int insertedCount = ps.executeUpdate();
if (insertedCount > 0)
{
  ResultSet generatedKeys = ps.generatedKeys();
  if (generatedKeys.next())
    generatedKeys.getInt(1);
}
```
