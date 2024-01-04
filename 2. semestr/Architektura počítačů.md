
## (cv 8) Periférie počítačů - vstupní zařízení - základní pricipy a funkce, Úvod do programování mikroprocesorů AVR

Tento kód ovládá sérii osmi LED diod pomocí spínače. Po spuštění programu vstoupí do funkce `setup()`, která nastaví piny LED diod jako výstupy a pin spínače jako vstup s interním pull-up rezistorem.

Poté přechází do nekonečné smyčky `loop()`, kde se kontinuálně kontroluje stav spínače. Pokud je spínač stisknut, postupně se rozsvěcují všechny LED diody a poté se zhasínají. Pokud spínač není stisknut, opačným směrem se postupně rozsvěcují a zhasínají LED diody. Tím vytváří efekt běhu světla do jednoho a opačného směru.

Celý kód se opakuje stále dokola, dokud je program spuštěn a nebyl přerušen nebo resetován.
````c++
int ledPin[] = {A1, 11, 12, 13, A0, 8, 9, 10}; // definice pinů pro LED
int switchPin = A3;                            // pin pro spínač

void setup()
{
  for (int i = 0; i < 8; i++){
    pinMode(ledPin[i], OUTPUT); // nastavení pinů LED jako výstupy
  }
 pinMode(switchPin, INPUT_PULLUP); // nastavení pinu spínače jako vstup s interním pull-up rezistorem
} 

void loop()
{
  if (digitalRead(switchPin) == LOW)
  { // pokud je spínač stisknut
    for (int i = 0; i < 8; i++)
    {
      digitalWrite(ledPin[i], HIGH); // rozsvítí všechny LED
      delay(100);                    // počká 100 ms
      digitalWrite(ledPin[i], LOW);  // zhasne všechny LED
    }
  }else
  { // pokud spínač není stisknut
    for (int i = 7; i >= 0; i--)
    {                                // zmena smeru behu
      digitalWrite(ledPin[i], HIGH); // rozsvítí LED na pozici i
      delay(100);                    // počká 100 ms
      digitalWrite(ledPin[i], LOW);  // zhasne LED na pozici i
    }
  }
}
````
----
## (cv 9) Periférie počítačů - výstupní zařízení - princip a funkce. Základy programování mikroprocesorů AVR

### Matice *(matrix)*
Tento kód vytváří matici s proměnnou velikostí a vypočítává její minimální a maximální hodnotu. Uživatel je vyzván k zadání velikosti matice a poté se vygeneruje a vypíše na sériový port. Následně jsou vypsány minimální a maximální hodnota matice. Kód také obsahuje příkazy pro blikání vestavěné LED diody s periodou jedné sekundy. Celý proces se opakuje v nekonečné smyčce `loop()`.

````c++
const int MAX_SIZE = 10;
int matrix[MAX_SIZE][MAX_SIZE];
  
void setup() {
    Serial.begin(9600);
    pinMode(LED_BUILTIN, OUTPUT);
}

void loop() {
    int size = 0;

    while (true) {
        Serial.print("Enter matrix size (3-10): ");
        while (!Serial.available());
        size = Serial.parseInt();
        if (size >= 3 && size <= MAX_SIZE) {
            break;
        }
        Serial.println("Invalid size!");
    }
 

    for (int i = 0; i < size; i++) {
        for (int j = 0; j < size; j++) {
            matrix[i][j] = i * size + j;
        }
    }

    int minVal = matrix[0][0];
    int maxVal = matrix[0][0];
    for (int i = 0; i < size; i++) {
        for (int j = 0; j < size; j++) {
            if (matrix[i][j] < minVal) {
                minVal = matrix[i][j];
            }
            if (matrix[i][j] > maxVal) {
                maxVal = matrix[i][j];
            }
        }
    }

    Serial.println("Matrix:");
    for (int i = 0; i < size; i++) {
        for (int j = 0; j < size; j++) {
            Serial.print(matrix[i][j]);
            Serial.print('\t');
        }
        Serial.println();
    }
  

    Serial.print("Min: ");
    Serial.println(minVal);
    Serial.print("Max: ");
    Serial.println(maxVal); 

    digitalWrite(LED_BUILTIN, HIGH);
    delay(1000);
    digitalWrite(LED_BUILTIN, LOW);
    delay(1000);
}
````
**takhle by to mělo vypadat podle toho leaked zadání, od -30 do 30** 
````c++
for (int i = 0; i < size; i++) {
  for (int j = 0; j < size; j++) {
    matrix[i][j] = random(-30, 31);
  }
}
````

### Rozklad prvočísla
Tento kód čte čísla ze sériového portu a provádí jejich rozklad na prvočísla. Po inicializaci sériové komunikace v `setup()` funkci se v nekonečné smyčce `loop()` kontroluje, zda jsou k dispozici data na sériovém portu. Pokud jsou, číslo je přečteno pomocí `Serial.parseInt()` a uloženo do proměnné `n`. Následně se provede rozklad čísla `n` na prvočísla.

V cyklu `for` se postupně prochází všechna čísla od 2 do `n`. Pokud je číslo `n` dělitelné beze zbytku číslem `i`, pak se `i` vypíše na sériový port. Před vypsáním dalšího prvočísla se vypíše oddělovací symbol (`*`). Proměnná `n` se dělí číslem `i`, aby se pokračovalo v rozkladu zbytku čísla.

Pokud nebylo nalezeno žádné prvočíslo (proměnná `first` zůstává `true`), pak je číslo `n` samo o sobě prvočíslem, a to se vypíše na sériový port. Na konci každého zpracování čísla se vypíše prázdný řádek pro oddělení výpisů různých čísel. Celý proces se neustále opakuje v nekonečné smyčce `loop()`.

#### Řešení 1
````c++
void setup() {
  Serial.begin(9600); // Inicializace sériové komunikace s rychlostí 9600 baudů
}

void loop() {
  if (Serial.available()) { // Pokud jsou k dispozici data na sériovém portu
    int n = Serial.parseInt(); // Přečti celé číslo ze sériového portu a ulož do proměnné n
    Serial.print(n); // Vypiš číslo na sériový port
    Serial.print(" = ");

    bool first = true; // Příznak pro označení prvního prvočísla v rozkladu
    for (int i = 2; i <= n; i++) { // Procházej všechna čísla od 2 do n
      while (n % i == 0) { // Pokud je n dělitelné beze zbytku i
        if (!first) { // Pokud nejde o první prvočíselný rozklad
          Serial.print("*"); // Vypiš hvězdičku jako oddělovač prvočísel
        }
        Serial.print(i); // Vypiš prvočíslo na sériový port
        n /= i; // Poděl číslo n prvočíslem i
        first = false; // Nastav příznak first na false, protože jsme již našli prvočíselný rozklad
      }
    }

    if (first) { // Pokud bylo číslo n rovno 1, znamená to, že se jedná o prvočíslo
      Serial.print("je prvocislo"); // Vypiš informaci, že číslo je prvočíslo
    }

    Serial.println(); // Vypiš nový řádek na sériový port pro oddělení výpisů různých čísel
  }
}
````
#### Řešení 2
````c++
unsigned int vstup;

bool jePrvocislo(int num) {
  if (num < 2) {
    return false;
  }

  for (int i = 2; i <= sqrt(num); i++) {
    if (num % i == 0) {
      return false;
    }
  }

  return true;
}

void rozkladCisla(int cislo) {

  if (jePrvocislo(cislo)) {
    Serial.print(cislo);
    Serial.println(" je prvočíslo");

  } else {

    int delitel = 2;
    Serial.print(cislo);
    Serial.print("=");
    while (cislo > 1) {
      if (cislo % delitel == 0) {
        Serial.print(delitel);
        cislo /= delitel;
        if (cislo > 1) {
          Serial.print("*");
        }
      } else {
        delitel++;
      }
    }
  }
}

void setup() {
  Serial.begin(9600);
}

void loop() {

  Serial.println("Zadejte číslo (max 9999): ");
  while (Serial.available() == 0) {}
  if (Serial.available()) {
    vstup = Serial.readString().toInt();
    if (vstup > 1 && vstup <= 9999) {
      rozkladCisla(vstup);
      Serial.println();
      Serial.println("_");
    } else {
      Serial.println("Neplatné číslo.");
    }
  }
}
````
----
## (cv 10) Datová uložiště - principy a funkce. Základy programování mikrokontrolérů AVR

Po obdržení hodnoty A od uživatele (state = 0) se zobrazí na displeji text "Zadej A:". Podobným způsobem se postupuje i pro hodnoty B (state = 1) a C (state = 2). Uživatel zadá hodnoty jednotlivých koeficientů kvadratické rovnice přes sériovou komunikaci.

Poté (state = 3) program vypočítá diskriminant (d) kvadratické rovnice pomocí vzorce b * b - 4 * a * c. Na základě hodnoty diskriminantu se výsledek zobrazí na sériovém monitoru. Pokud je diskriminant menší než 0, vypíše se, že kvadratická rovnice nemá reálné kořeny. Pokud je diskriminant roven 0, vypíše se, že kvadratická rovnice má jeden kořen, a vypočítaný kořen (x1) se zobrazí. Pokud je diskriminant větší než 0, vypíše se, že kvadratická rovnice má dva kořeny, a vypočítané kořeny (x1 a x2) se zobrazí.

Poté se stav (state) nastaví zpět na 0 a program opět čeká na další vstup od uživatele pro hodnotu A. Tento proces se opakuje v nekonečné smyčce loop().
````c++
#include "Native_LiquidCrystal.h"
#include "math.h"

// Definice komunikacnich pinu. Zde je potreba dat pozor na datove piny, protoze UnoArduSim

// ma pouze jedno okenko pro nejnizsi dat. pin (DB4) a potom bere, ze dalsi tri nasledujici piny jsou DB5, DB6 a DB7.

// Take je mozne vynechat pin R/W - coz delam, proto?e muj realny displej ho ma natvrdo na GND.

#define RS_PIN 7
#define EN_PIN 6
#define D4_PIN 2
#define D5_PIN 3
#define D6_PIN 4
#define D7_PIN 5

Native_LiquidCrystal lcd(RS_PIN, EN_PIN, D4_PIN, D5_PIN, D6_PIN, D7_PIN);
void setup(){

  lcd.begin(16, 2);
  lcd.setCursor(0, 0);
  lcd.print("Kvadraticke rovnice:");
  lcd.setCursor(0, 1);
  lcd.print("Malinda Krystof");
  Serial.begin(9600);
}

void loop() {
  static int state = 0;
  static float a, b, c, x1, x2, d;
  if (state == 0) {
    lcd.clear();
    lcd.setCursor(0, 0);
    lcd.print("Zadej A:");
    Serial.println("Zadej A:");
    while (Serial.available() == 0) {
    }
    a = Serial.parseFloat();
    state = 1;
  } else if (state == 1){
    lcd.clear();
    lcd.setCursor(0, 0);
    lcd.print("Zadej B:");
    Serial.println("Zadej B:");
    while (Serial.available() == 0) {
    }
    b = Serial.parseFloat();
    state = 2;

  }else if (state == 2){
    lcd.clear();
    lcd.setCursor(0, 0);
    lcd.print("Zadej C:");
    Serial.println("Zadej C:");
    while (Serial.available() == 0) {
    }
    c = Serial.parseFloat();
    state = 3;
  } else if (state == 3)

  {
    lcd.clear();
    d = b * b - 4 * a * c;
    if (d < 0){
      Serial.println("Kvadratická rovnice nemá reálné koreny");
    
    } else if (d == 0){
      x1 = x2 = -b / (2 * a);
      Serial.print("Kvadratická rovnice má jeden koren: ");
      Serial.println(x1);
    
    } else{
      x1 = (-b + sqrt(d)) / (2 * a);
      x2 = (-b - sqrt(d)) / (2 * a);
      Serial.print("Kvadratická rovnice má dva koreny: ");
      Serial.print(x1);
      Serial.print(", ");
      Serial.println(x2);
    }
    state = 0;
  }
}
````
