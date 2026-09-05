```Java
public class Team<T extends Player>    // Has to be a Player or a sub-class of it
                                      // leading to call methods other than the Object class
{

  private List<T> players;

  public void m()
  {
    players.<Player type functionality>,
  }
}
```
