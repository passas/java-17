```Java
public interface MyInterface implements OtherInterface, AnOtherInterface
{
  public static final int I = 1;
  int J = 1;

  public abstract void f();
  void m();

  // jdk-8              -- in order to not break already implemented classes
  default Object n()
  { return null; }

  // jdk-9
  private int i = -1;
  
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

  @Override
  public void n()
  { return new Object() }

}
```
