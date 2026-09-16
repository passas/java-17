```Java
// (IN ..., IN ..., IN ..., OUT ...)

CallableStatement cs = connection.callableStatement("call x.y(?,?,?,?)");
cs.set...(1, ...);
cs.set...(2, ...);
cs.set...(3, ...);
cs.registerOutParameter(4, Types.INTEGER);
cs.execute();

cs.getInt(4);
```

```Java
// (IN ..., IN ..., IN ..., INOUT ...)

CallableStatement cs = connection.callableStatement("call x.y(?,?,?,?)");
cs.set...(1, ...);
cs.set...(2, ...);
cs.set...(3, ...);
cs.set...(4, ...);
cs.registerOutParameter(4, Types.INTEGER);
cs.execute();

cs.getInt(4);
```
