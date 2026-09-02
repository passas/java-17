```Java
int i = 0;
{
  int j = 1;
  System.out.println(i);
  System.out.println(j);
}
System.out.println(i);
System.out.println(j); // error
```

Derp:
```Java
switch(expression)
{
  case match:
    int i = 0;
    break;
  case match:
    System.out.println(i);
    System.out.println(j);  // error
  default:
    int j = 1;
}
```
