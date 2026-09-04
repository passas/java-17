As a cursor on DB systems

```Java
void iterate(List<Object> list)
{
  var iterator = list.iterator();
  while(iterator.hasNext())
  {
    Object object = iterator.next();
  }
}
```


```Java
void empty(List<Object> list)
{
  var iterator = list.iterator();
  while(iterator.hasNext())
    iterator.remove();
}
```
