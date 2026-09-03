```Java
public class MyClass
{
  Integer i;
  Integer j;

  public MyClass()
  {
    this(null, null);
  }

  public MyClass(Integer i)
  {
    this(i, null);
  }

  public MyClass(Integer i, Integer j)
  {
    this.i = i;
    this.j = j;
  }
}
```
