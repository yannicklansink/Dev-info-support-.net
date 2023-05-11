
```csharp
public class SpelerRepository : ISpelerRepository
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
