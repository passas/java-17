```Java
@FunctionalInteface
public interface Operation<T>
{
  T operate(T value1, T value2);
}
```

```Java
public <T> T calculator(Operation<T> function, T value1, T value2)
{
  T result = function.operate(value1, value2);
  return result;
}

int r = calculator((a,b) -> a + b, 5, 2);
```
