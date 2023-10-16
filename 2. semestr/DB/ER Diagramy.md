## První
![DB](2.%20semestr/DB/diagramy/první.png)

```sql
CREATE TABLE ÚSTAV(
id_úst PRIMARY KEY,
název_ust VARCHAR(255) NOT NULL,
adresa VARCHAR(255) NOT NULL
);
```

```sql
CREATE TABLE ODBOR(
c_odb PRIMARY KEY,
nazev_odb VARCHAR(255) NOT NULL,
id_úst INT NOT NULL REFERENCES ÚSTAV(id_úst),
);
```

```sql
CREATE TABLE KANCELÁŘ(
název_kanc VARCHAR(100) NOT NULL PRIMARY KEY,
telefon VARCHAR(13) NOT NULL,
id_úst INT NOT NULL REFERENCES ÚSTAV(id_úst),
c_odb INT REFERENCES ODBOR(c_odb)
);
```

## Druhý
![DB](2.%20semestr/DB/diagramy/druhý.png)
```sql
CREATE TABLE KOMPONENTA(
id_komp PRIMARY KEY,
název VARCHAR(255) NOT NULL,
výrobce VARCHAR(255) NOT NULL
);
```

```sql
CREATE TABLE VÝROBEK(
id_výrobku PRIMARY KEY NOT NULL REFERENCES id_komp,
název VARCHAR(255) NOT NULL,
POPIS VARCHAR(255) NOT NULL
)
```
## Třetí
![DB|750](2.%20semestr/DB/diagramy/třetí.png)
````SQL
CREATE TABLE ZAMĚSTNANEC(
č_zam PRIMARY KEY,
jméno VARCHAR(255) NOT NULL,
narozen DATE
);
````

```SQL
CREATE TABLE SPRÁVNÍ_RADA(
id_rady PRIMARY KEY NOT NULL REFERENCES č_zam,
organizace VARCHAR(255) NOT NULL,
POPIS VARCHAR(255) NOT NULL
);
```

