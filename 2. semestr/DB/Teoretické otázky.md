1. **Co to je SW inženýrství a k čemu je dobré?**

   Software Engineering (SW inženýrství) je disciplína zabývající se systematickým návrhem, vývojem, provozem a údržbou softwarových systémů. Cílem SW inženýrství je aplikovat inženýrské principy a postupy na vývoj software, aby byl spolehlivý, efektivní, udržitelný a splňoval požadavky uživatelů.

2. **Co to je životní cyklus SW, jaké modely například znáte?**

   Životní cyklus softwaru (Software Development Life Cycle - SDLC) je soubor fází a aktivit, které se provádějí při vývoji a správě softwaru. Existuje mnoho modelů životního cyklu softwaru, z nichž některé jsou: vodopádový model, iterativní model, prototypování, inkrementální model, spirálový model, agilní metodiky (SCRUM, Kanban atd.).

3. **Jaké základní fáze má životní cyklus SW?**

   Základní fáze životního cyklu softwaru jsou:

   - Analýza požadavků
   - Návrh
   - Implementace
   - Testování
   - Nasazení
   - Údržba

4. **Jaké znáte druhy DBMS?**

   Základními druhy DBMS (Database Management System) jsou:

   - Relační databáze
   - Hierarchické databáze
   - Síťové databáze
   - Objektově orientované databáze
   - Dokumentové databáze
   - NoSQL databáze

5. **Co to je transakce, k čemu je dobrá?**

   Transakce je logická jednotka práce v databázovém systému. Transakce slouží k provedení souboru operací nad databází jako jednotnou a atomickou akci, která buď proběhne úspěšně a změny se uloží, nebo se žádné změny neprovedou. Transakce zajistí konzistenci a integritu dat a zajišťují, že změny provedené v rámci transakce se provedou buď kompletně, nebo vůbec.

6. **Co znamená, že data v DB jsou spolehlivá?**

   Spolehlivá data v databázi znamenají, že jsou přesná, konzistentní a dostupná ve správném formátu a čase. Spolehlivost dat je zajištěna pomocí mechanismů jako jsou zálohy, redundance dat, validace vstupů, kontroly integrity dat a dalších opatření pro minimalizaci chyb a ztrát dat.

7. **Co znamená, že data v DB jsou neredundantní?**

   Neredundantní data v databázi znamenají, že každá informace je uložena pouze jednou, aby se minimalizovala redundance a duplicita dat. Tím se zlepšuje efektivita uložení dat, snižuje se riziko nesouladu dat a zajišťuje se jednoznačnost a konzistence informací.

8. **Co to je konceptuální model a k čemu je dobrý?**

   Konceptuální model je abstraktní reprezentace struktury a vztahů mezi entitami v daném systému. Slouží k vizualizaci a popisu konceptuálního návrhu informačního systému, nezávisle na konkrétní implementaci. Pomáhá analytikům a vývojářům porozumět požadavkům, provádět analýzu, komunikovat s klienty a navrhovat správné řešení.

9. **Jaké má konceptuální model obvykle součásti?**

   Konceptuální model obvykle zahrnuje:

   - Entitní typy a jejich atributy
   - Vztahy mezi entitními typy
   - Kardinalitu vztahů
   - Specifikace klíčů
   - Další omezení a pravidla

10. **Co to je integritní omezení?**

    Integritní omezení jsou pravidla a podmínky, které definují platnost a konzistenci dat v databázi. Tyto omezení omezují neplatné hodnoty, vztahy nebo operace a zajišťují, že data jsou v souladu s definovanými pravidly a požadavky.

11. **Co to je kandidátní klíč v konceptuálním modelu?**

    Kandidátní klíč je atribut nebo kombinace atributů, které jednoznačně identifikují entitu v konceptuálním modelu. Slouží jako potenciální kandidáti pro primární klíč a musí splňovat podmínky jednoznačnosti a minimality.

12. **Porovnejte případy použití přirozeného a umělého identifikátoru, jmenujte výhody a nevýhody.**

    - Případ použití přirozeného identifikátoru:
      - Přirozený identifikátor je atribut, který již existuje v datech a má význam pro uživatele.
      - Výhody: Jednoduchá identifikace, snadná čitelnost, přirozený vztah k entitě.
      - Nevýhody: Omezená flexibilita, změna hodnoty může být obtížná nebo nemožná.

    - Případ použití umělého identifikátoru:
      - Umělý identifikátor je speciální atribut, který je přidělován entitě a nemá žádný vztah k přirozeným datům.
      - Výhody: Unikátnost, snadná změna hodnoty, flexibilita.
      - Nevýhody: Může být nečitelný pro uživatele, vyžaduje další atribut pro identifikaci entity.
13. **Jaká IO mohou mít atributy?**

    Atributy mohou mít následující IO (identifikační omezení):

    - Primární klíč (PK): Jedinečně identifikuje každý záznam v tabulce.
    - Cizí klíč (FK): Slouží k vytvoření vztahu mezi dvěma tabulkami na základě hodnoty v jiné tabulce.
    - Unikátní hodnota (UNIQUE): Omezuje hodnoty atributu na unikátní hodnoty v rámci tabulky.
    - Defaultní hodnota: Určuje implicitní hodnotu, která se použije, pokud není hodnota specifikována.
    - Not null: Vyžaduje, aby atribut měl vždy vyplněnou hodnotu.

14. **Jaká IO mohou mít vztahy?**

    Vztahy mezi tabulkami mohou mít následující IO:

    - Primární cizí klíč (PK-FK): Slouží k propojení primárního klíče jedné tabulky s cizím klíčem druhé tabulky.
    - Jednostranný vztah: Vztah mezi dvěma tabulkami, kde jedna tabulka odkazuje na druhou, ale ne naopak.
    - Vícestranný vztah: Vztah, ve kterém se podílejí více než dvě tabulky.
    - Omezení vztahu: Definuje, jaké operace jsou povoleny mezi propojenými tabulkami (např. ON DELETE CASCADE, ON UPDATE SET NULL).

15. **Co to je slabý entitní typ, jak s tím souvisí pojem částečný klíč?**

    Slabý entitní typ je entita, která nemůže existovat samostatně, ale musí být vždy spojena s jinou entitou pomocí vztahu. Slabé entity mají vlastní identifikátor, který se nazývá částečný klíč. Částečný klíč se skládá ze části primárního klíče slabé entity a části primárního klíče silné entity, ke které je slabá entita připojena.

16. **Co to je rekurzivní typ vztahu?**

    Rekurzivní typ vztahu je situace, kdy entita navazuje vztah sama na sebe. To se často používá pro modelování hierarchických struktur nebo stromů. V takovém případě se používá jedna tabulka, ve které je atribut, který odkazuje na primární klíč stejné tabulky.

17. **Co to je ISA hierarchie, jak je definována?**

    ISA hierarchie (také známá jako dědičnost nebo generalizace-specifikace) je modelovací technika, která popisuje vztah mezi nadřazenou (rodičovskou) a podřazenou (potomkovskou) entitou. Hierarchie se definuje pomocí vztahu "je druhem" (is-a relationship), kde podřazená entita je specifickým případem nadřazené entity. Hierarchie se často používá k modelování dědičnosti v objektově orientovaném programování.

18. **Co to je výlučný typ vztahu?**

    Výlučný typ vztahu je situace, kdy entita může být spojena pouze s jednou entitou z jiné tabulky a toto spojení je vyloučeno s ostatními entitami v této tabulce. Jedná se o speciální případ vztahu s omezeným rozsahem, který se používá k modelování vztahů, kde je nutné zajistit, že entita je propojena pouze s jedním specifickým záznamem z jiné tabulky.

19. **Jakými způsoby lze dekomponovat vztah M:N, jak se identifikuje nová entita?**

    Vztah M:N lze dekomponovat následujícími způsoby:

    - Použitím nové entity: Vytvoření nové entity, která reprezentuje vztah mezi dvěma entitami M:N. Tato nová entita bude obsahovat primární klíče obou entit jako cizí klíče a může také obsahovat další atributy specifické pro tento vztah.
    - Použitím dvou vztahů 1:N: Rozdělení vztahu M:N na dva vztahy 1:N mezi třemi entitami. Každý vztah bude mít cizí klíč jedné z entit jako svůj atribut.

20. **Co to je relace (matematicky), jak souvisí s DB?**

    V matematice je relace kolekce uspořádaných dvojic hodnot, která může mít různé vlastnosti. V kontextu databázových systémů je relace základním prvkem relačního modelu. Relace v DB představuje tabulku, která se skládá z řádků a sloupců, přičemž každý řádek představuje záznam a každý sloupec představuje atribut.

21. **Jaké jsou základní operace nad relačním modelem?**

    Základní operace nad relačním modelem zahrnují:

    - SELECT: Slouží k vybrání určitých řádků a sloupců z relace na základě zadaných podmínek.
    - PROJECT: Slouží k vybrání určitých sloupců z relace a odstranění duplicity.
    - JOIN: Slouží k propojení dvou nebo více relací na základě společného atributu.
    - UNION: Slouží k spojení dvou relací, přičemž výsledkem je relace obsahující unikátní záznamy z obou relací.
    - INTERSECT: Slouží k nalezení společných záznamů ve dvou relacích.
    - DIFFERENCE: Slouží k nalezení rozdílu mezi dvěma relacemi.

22. **Co to je 1. normální forma?**

    První normální forma (1NF) je základním požadavkem pro správnou strukturu relačního modelu. Splnění 1NF vyžaduje, aby každý atribut v tabulce obsahoval pouze atomické (nedělitelné) hodnoty. To znamená, že žádný atribut by neměl obsahovat seznam hodnot nebo složené hodnoty. Dále se vyžaduje, aby každý řádek v tabulce byl jednoznačně identifikován primárním klíčem.

23. **Co to je referenční integrita?**

    Referenční integrita je vlastnost relačního modelu, která zajišťuje konzistenci dat při používání cizích klíčů. Referenční integrita definuje pravidla pro vazby mezi tabulkami a zabraňuje vzniku nekonzistentních datových vztahů. Například, pokud existuje vztah mezi dvěma tabulkami pomocí cizího klíče, referenční integrita zajistí, že nebudou povoleny operace, které by porušily tento vztah, jako je například odstranění záznamu z nadřazené tabulky, na který se odkazuje záznam v podřazené tabulce.

24. **Co to je klíč relačního schématu?**

    Klíč relačního schématu je atribut nebo kombinace atributů, které jednoznačně identifikují každý záznam v tabulce. Klíč slouží k identifikaci a propojení záznamů v rámci tabulky a mezi tabulkami. Primární klíč je speciální typ klíče, který je vybrán jako hlavní identifikátor pro tabulku. Cizí klíč je klíč, který odkazuje na primární klíč jiné tabulky a slouží k vytvoření vztahu mezi tabulkami.


