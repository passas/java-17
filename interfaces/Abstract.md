*abstract* *static* *final* *default* *native* *synchronized*

```Java
public abstract class MyClass extends OtherClass
{
  protected int i;
  private int j;
  
  public MyClass()
  {
    super();
    this.i = 0;
    this.j = 0;
  }
  
  public abstract void f();

  protected abstract void h();

  abstract void m();

  public final void n()
  {
    statements
    this.m();
  }

  public void p()
  {
    this.n();
  }

}
```

```Java
public class MyOtherClass extends MyClass
{
  private int w;

  public MyOtherClass()
  {
    super();
    this.i = 1;
    this.w = 0;
  }

  @Override
  public void f()
  { statements }

  @Override
  public void h()
  { statements }

  @Override
  void m()
  { statements }

  @Override
  public void p()
  { statements }
}
```
