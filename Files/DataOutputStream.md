```Java
void writeData (File dataFile)
{

  try (DataOutputStream dataOutputStream = new DataOutputStream( new BufferedOutputStream ( new FileOutputStream ( dataFile.toFile() ) ) ) )
  {
    int myInt = 17;
    long myLong = 100_000_000_000L;
    bolean myBoolean = true;
    char myChar = 'z';
    float myFloat = 77.7f;
    double myDouble = 98.6;
    String myString = "Hello, world";

    long position = 0;

    dataOutputStream.writeInt(myInt);
    dataOutputStream.size() - position;  // occupies
    position = dataOutputStream.size();

    dataOutputStream.writeLong(myLong);
    dataOutputStream.size() - position;  // occupies
    position = dataOutputStream.size();

    dataOutputStream.writeBoolean(myBoolean);
    dataOutputStream.size() - position;  // occupies
    position = dataOutputStream.size();

    dataOutputStream.writeChar(myChar);
    dataOutputStream.size() - position;  // occupies
    position = dataOutputStream.size();

    dataOutputStream.writeFloat(myFloat);
    dataOutputStream.size() - position;  // occupies
    position = dataOutputStream.size();

    dataOutputStream.writeDouble(myDouble);
    dataOutputStream.size() - position;  // occupies
    position = dataOutputStream.size();

    dataOutputStream.writeUTF(myString);
    dataOutputStream.size() - position;  // occupies
    position = dataOutputStream.size();
    
  }
  catch (FileNotFoundException e)
  {}
  catrch (IOException e)
  {}
}
```
