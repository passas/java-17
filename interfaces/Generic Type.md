T, S, U, V := types

E := element

K := key

V := values

Enforce type check at compile time:
```Java
public class Team<T>
{
  private List<T> players;

  public Team()
  {
    this.players = new ArrayList<>();
  }

  private void addPlayer(T t)
  {
    this.players.add(t);
  }
}
```
