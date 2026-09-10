```Java
public class MyClass implements Serializable
{
}
```

```Java
void writeObject (Path dataFile, MyClass object)
{
  try( ObjectOutputStream oos = new ObjectOutputStream ( Files.newOutputStream ( dataFile ) ) )
  {
    oos.writeObject(object);
  }
  catch(FileNotFoundException e)
  {}
  catch(IOException e)
  {}
}
```

```Java
MyClass readObject (Path dataFile)
{
  try( ObjectInputStream ois = new ObjectInputStream ( Files.newInputStream ( dataFile ) ) )
  {
    return (MyClass) ois.readObject();
  }
  catch(FileNotFoundException e)
  {}
  catch(IOException | ClassNotFoundException e)
  {}
}
```

.dat

```Java
private static final long serialVersionUID = 1L;
```
