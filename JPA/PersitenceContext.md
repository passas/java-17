```Java
        try  (var sessionFactory =
                Persistence.createEntityManagerFactory(
                        "dev.lpa.music" );
              EntityManager entityManager = sessionFactory.createEntityManager();
        ) {

            var transaction = entityManager.getTransaction();
            transaction.begin();
            Artist artist = entityManager.find(Artist.class, 202);
            artist.setArtistName("Muddy Waters");
            System.out.println(artist);
//            entityManager.remove(artist);
//            entityManager.persist(new Artist("Muddy Water"));
            transaction.commit();
        } catch (Exception e) {
            e.printStackTrace();
        }

```
