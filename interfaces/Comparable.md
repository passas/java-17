```Java
public interface Comparable<T>
{
  public int compareTo(T t); // < 0 ; == 0 ; > 0
}
```

```Java
public class Student implements Comparable<Student>
{
  private String name;

  int compareTo(Student s)
  {
    return this.name.compareTo(s.name);      
  }

}
```
