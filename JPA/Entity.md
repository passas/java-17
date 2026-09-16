```Java
@Entity
@Table(name = "artists")
public class Artist
{
  @Id
  @GeneratedValue(strategy = GeneratedValue.IDENTITY)
  @Column(name="artist_id")
  private int artistId;

  @Column("artist_name")
  private String artistName;

  @OneToMany
  @JoinColumn(name="artist_id")
  private List<Album> albums = new ArrayList<>();
}
```
