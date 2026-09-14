```Java
void transaction(Connection conenction)
{
  connection.setAutoCommit(false);
  try
  {
    ...
    connection.commit();
  }
  catch(SQLException e)
  {
    connection.rollback();
  }
  connection.setAutoCommit(true);
}
```

Batch:
```Java
// connectionString?continueBatchOnError=false

void transaction(Connection conenction)
{
  connection.setAutoCommit(false);
  try
  {
    ...
    statement.addBatch(...);
    statement.addBatch(...);
    int[] results = statement.executeBatch();
    connection.commit();
  }
  catch(SQLException e)
  {
    connection.rollback();
  }
  connection.setAutoCommit(true);
}
```
