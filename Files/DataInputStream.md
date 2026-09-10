```Java
void readData (File dataFile)
{

  //try (DataInputStream dataInputStream = new DataInputStream( new BufferedInputStream ( new FileInputStream ( dataFile.toFile() ) ) ) )
  try (DataInputStream dataInputStream = new DataInputStream( Files.newInputStream( dataFile ) ) ) 
  {
    dataInputStream.readInt();
    dataInputStream.readLong();
    dataInputStream.readBoolean();
    dataInputStream.readChar();
    dataInputStream.readFloat();
    dataInputStream.readDouble();
    dataInputStream.readUTF();
  }
  catch (FileNotFoundException e)
  {}
  catrch (IOException e)
  {}
}
```
