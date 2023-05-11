
```csharp
public class SpelerRepository : ISpelerRepository
{
	public void NieuweSpelerToevoegen(Speler speler)
    {
            using (var context = new BlackJackDbContext(_options))
            {
                context.Spelers.Add(speler); // Expliciet aangeven dat het om de Spelers tabel gaat
                context.SaveChanges();
            }
    }
}

```

DAL = Data Acces Layer (Ook wel een DAO genoemd(Data Access Object))

```csharp
public interface ISpelerRepository
    {
        IEnumerable<Speler> GetAllSpelers();
        
        Speler GetSpelerById(long id);

        Speler GetSpelerByNaam(String naam);

        void NieuweSpelerToevoegen(Speler speler);

        void SpelerUitschrijven(Speler speler);

        void SpelerSaldoAanpassen(Speler speler);


    }
```
