```Java
String CONNECTION_STRING = "jdbc:mysql://127.0.0.1:3306/<db>";
String user = "<user>";
String password = "<password>";
```

DriverManager:
```Java
try(Connection connection = DriverManager.getConnection(CONNECTION_STRING, user, password))
{
}
catch(SQLException e)
{
}
```

DataSource:
```Java
var dataSource = new MysqlDataSource();
dataSource.setUrl(CONNECTION_STRING);
try(Connection connection = dataSource.getConnection(user, password))
{
}
catch(SQLException e)
{
}
```

```Java
var dataSource = new MysqlDataSource();
dataSource.setServerName("localhost");
dataSource.setPort(3306);
dataSource.setDatabaseName("<db_name>");
try(Connection connection = dataSource.getConnection(user, password))
{
}
catch(SQLException e)
{
}
```
