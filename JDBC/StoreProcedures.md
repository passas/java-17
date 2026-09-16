```Java
CallableStatement cs = connection.prepareCall("CALL music.addAlbum(?,?,?)");
cs.setString(1, ...);
cs.set...(2, ...);
cs.set...(3, ...);
cs.execute();
```
