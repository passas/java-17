```Java
public interface MyInterface implements OtherInterface, AnOtherInterface
{
  public abstract void f();
  void m();
}
```

```Java
public class MyClass implements MyInterface
{
  private int i = 0;
  public MyClass()
  {
    this.i = 0;
  }

  @Override
  public void f()
  { statements }

  @Override
  public void m()
  { statements }
}
```
