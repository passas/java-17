```Java
public class Team<T extends Player & FootballPlayer>    // Has to be a Player or a sub-class of it, as also a FootballPlayer (interface)
                                                        // leading to call methods other than the Object class
{

  private List<T> players;

  public void m()
  {
    players.<Player type functionality>,
  }
}
```


```Java
public class Team<T extends Player, S>   
{
  private S affiliation;
  private List<T> players;
}
```

```Java
// Generic Method
public <T> void p(List<T> t)
{
  System.out.println(t.join("\n", t));
}

// Generic Method
public <T extends Player> void p(List<T> t)
{
  System.out.println(t.join("\n", t));
}

// Wildcard
public void p(List<? extends Player> t)    // Player or sub-type
{
  System.out.println(t.join("\n", t));
}

public void p(List<? super Player> t)      // Player or parent
{
  System.out.println(t.join("\n", t));
}
```

Widlcard
```Java
public void print(List<?> list)
{
  for (var element : list)
    if (element instanceof String s)
        s.toUpperCase();
    else if (element instanceof Integer i)
        i.floatValue();
}
```
