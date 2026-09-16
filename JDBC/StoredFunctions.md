```Java
CallableStatement csf = connection.prepareCall("{ ? = CALL music.calcAlbumLength(?) }");
csf.registerOutParameter(1, Types.DOUBLE);
csf.setString(2, ...);
csf.execute();

csf.getDouble(1);
```
