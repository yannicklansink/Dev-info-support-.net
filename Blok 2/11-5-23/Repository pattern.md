Dit is eigenlijk een data mapper
Want je gebruikt een context in je methode.
Een repository is een class die alle logica bevat voor het werken met de database.
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

## Data mapper vs repository
- Data mapper blijft korter verbonden met de DB
- Data mapper wordt soms ook repository genoemd, maar is het niet.
- In praktijk wordt vaker de repository gebruikt.
- context maak je niet meer in de methode, maar in de class zelf.