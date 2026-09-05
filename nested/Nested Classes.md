```Java
public class MyClass
{
  public static class MyClassComparator <T extends MyClass> implements Comparator<MyClass>
  {
    @Override
    public int compareTo(MyClass m1, MyClass m2)
    {
      return (int) (m1.field - m2.field);
    }
  }
}
```

```Java
List<MyClass> list;

list.sort(new MyCLass.MyClassComparator<>());
list.sort(new MyCLass.MyClassComparator<>().reversed());
```
