\>= JDK-14

Immutable;

private final fields;

public full constructor;

public getters; ( student.name(); )

public formatted toString.


```Java
public record Student(String id, String name, String dateOfBirth, String classList)
{}
```


```Java
public record Student(String id, String name, String dateOfBirth, String classList)
{
  public Student(String id)
  {
    this(id, null, null, null);
  }
}
```
