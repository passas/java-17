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
  }
  catch (FileNotFoundException e)
  {}
  catrch (IOException e)
  {}
}
```
