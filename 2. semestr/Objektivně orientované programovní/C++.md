## Úvod
````c++
#include <iostream> //basic input/output operace
int main()
{
    // Toto je komentář
    /*
    multi line comment
    :)
    */
    std::cout << "I like burger!" << '\n';
    std::cout << "It's really good!" << '\n';
    return 0; // kdyz dojdeme sem tak je konec kodu nebo funkce
}
````
## Deklarace proměných
````c++
#include <iostream>

  

int main()

{

    int x; // deklarace
    // int x = 5; je taky způsob
    x = 5;
    int y = 6;
    int sum = x + y;

  

    // integer (whole number)
    int age = 21;
    int year = 2023;
    int days = 7;


    // double (number including decimal)
    double price = 100.99;
    double gpa = 2.5;
    double tax = 0.01;


    // char (single character)
    char grade = 'A';
    char initials = 'B';

  
    // boolean (true/false)
    bool is_male = true;
    bool is_female = false;


    // string (object that represents a sequence of text)
    std::string name = "Bro";
    std::string day = "Sunday";

    std::cout << "Hello " << name << '\n';
    return 0;

}
````
## Const
````c++
    // const dělá proměnou read only
    const double PI = 3.14159;
    // PI = 420.69; nejde tedy dále přepisovat
    double radius = 10;
    double circumference = 2 * PI * radius;
    std::cout << circumference << " cm";
    return 0;
````
## Namespace
````c++
#include <iostream>

  

namespace first
{
    int x = 1;
}

namespace second
{
    int x = 3;
}

  
int main()

{

    using namespace std; //kdyz dame toto tak nemusim davat std:: kdych chceme vypisovat ale je tam toho moc
    using std::count; // je bezpecnejsi
    using std::string; // je bezpecnejsi pro string
    int x = 0;

  

    std::cout << x; //nepouzije namespace
    std::cout << first::x; //pouzijese namespace first
    std::cout << second::x; //pouzije se namespace second

    return 0;

}
````
Namespace, dává řešení na prevenci konfliktův v pojmenování ve velkých projektech
Každá entita potřebuje unikátní jméno
A namespace dovoluje identicky jméné entity dokud jsou namespace jiné

## Typedef and type aliases
Vlastně typedef dává přezdívky nějakým data typům
a pojmenovaná se většinou zakončuje "podrzitko t"
Je to dobré aby se redukovali překlepy
Moc se to nevyplatí používat pokud nevidíme jasný benefit
````c++
#include <iostream>

  

//Toto je starsi
//typedef std::string text_t;
//typedef int number_t;

  

//Toto je vice popularni
using text_t = std::string;
using number_t = int;

  

int main()
{

    text_t firstName = "John";
    number_t age = 21;
  

    std::cout << age '\n';
    std::cout << firstName << '\n';

    return 0;

}
````
## Artmetické operace
Basic matematika

## Type conversion
Implicitní = automatická
Explicitní = nový  data typ
````c++
#include <iostream>

  

int main()

{

    /*
    int x = 3.14;
    prepiseme na
    double x = 3.14;


   Implicit conversion

    */

    double x = (int)3.14; // explicit type conversion

    int correct = 8;
    int question = 10;

    double score = correct / (double)question * 100;
    std::cout << score << " %" << std::endl;
    std::cout << x << std::endl;
    return 0;

}
````
Je to různe kde se to dá použít ale je dobré vedět že to existuje
````c++
#include <iostream>

  
  

int main()

{
    std::string name;
    int age;

  

    std::cout << "Enter your full name: " << '\n';
    std::getline(std::cin >> std::ws, name); // diky tomuto muzeme psat stringy s mezerami

    std::cout << "Enter your age: " << '\n';
    std::cin >> age;
    std::cout << "Hello, " << name << std::endl;
    std::cout << "You are " << age << " years old." << '\n';
    return 0;

}

  

//Problem vznika bez pouziti "std:ws"
````
---
## Cvičný program
Cvičný program pro výpočet třetí strany pravoúhlého trojúhelníku
````c++
#include <iostream>
#include <cmath>
  

int main()

{
    double a;
    double b;
    std::cout << "-------------------------------------------" << '\n';
    std::cout << "Program na výpočet pravouhleho trojuhelniku" << '\n';
    std::cout << '\n';
    std::cout << '\n';
    std::cout << "Zadej stranu a: ";
    std::cin >> a;
    std::cout << "Zadej stranu b: ";
    std::cin >> b;
    std::cout << '\n';
    // c = odmocnina z a na druhou + b na druhou
    double c = sqrt(pow(a, 2) + pow(b, 2));
    std::cout << "Vysledek je: " << c << '\n';
    std::cout << '\n';
    return 0;

}
````

## Ternary operator
````c++
#include <iostream>
int main()

{

    // ternary operator ?: = replacement to an if/else statement
    // condition ? expression1 : expression2


    int grade = 75;

    /* if(grade >= 60)
    {
        std::cout << "You pass!";
    }
    else
    {
        std::cout << "You fail!";
    }

  

    Takhle to je kdyz by to bylo if
*/

// A takhle ternanry operatorem
grade >= 60 ?  std::cout << "You pass!" : std::cout << "You fail!";
// kriterium ? pokud je true : pokud je false

  

int number = 9;
number % 2 ? std::cout << "OOD" : std::cout << "EVEN";
  

bool hungry = true;
hungry ? std::cout << "Hungry" : std::cout << "Not hungry";

  

    return 0;

}
````
## Logické operátory
````c++
#include <iostream>

int main

{

    // && = Pokud je obojí pravda
    // || = Pokud jedno z toho je pravda
    // ! = Neguje

    int temp;
	std:cout << "Enter the temperature: ";
    std::cin >> temp;

    if (temp > 0 && temp < 30)

    {
    // oboje musí být pravda aby to bylo true
    std:

       cout << "The temperatue is good!";

    }

    else

    {

        std::cout << "The temperatue is bad!";

    }

  

    return 0;

}
````
## Příklady na procvičení
1.  Kalkulačka: Naprogramujte jednoduchou kalkulačku, která bude schopna provádět základní matematické operace (sčítání, odčítání, násobení, dělení). Kalkulačka by měla být interaktivní a umožňovat uživateli zadávat vstupy. **HOTOVO**
    
2.  Hádání čísla: Naprogramujte hru, ve které počítač náhodně vybere číslo mezi 1 a 100 a hráč bude mít několik pokusů na to, aby uhodl toto číslo. Po každém pokusu počítač zobrazí hráči, zda jeho hádání bylo příliš vysoké nebo příliš nízké.
    
3.  Šifrování a dešifrování: Naprogramujte program pro šifrování a dešifrování textu pomocí Caesarovy šifry. Uživatel by měl mít možnost zadat klíč, který určí, o kolik písmen bude text posunut.
    
4.  Bankomat: Naprogramujte program, který simuluje chování bankomatu. Uživatel by měl mít možnost zadat své jméno a heslo k účtu, zkontrolovat svůj zůstatek a vybírat hotovost.
    
5.  Jednoduchá databáze: Naprogramujte jednoduchou databázi, která umožní ukládat a zobrazovat seznam studentů a jejich výsledků. Databáze by měla umožnit přidávat a mazat záznamy, stejně jako vyhledávat studenty podle jména.
    
6.  Křížovky: Naprogramujte hru křížovky, ve které hráč bude muset uhodnout slova na základě definic. Hra by měla obsahovat několik obtížností a umožňovat ukládání výsledků hráčů.
    
7.  Automat na nápoje: Naprogramujte automat na nápoje, který bude umožňovat uživatelům vybírat nápoje a platit za ně mincemi a bankovkami.
    
8.  To-do list: Naprogramujte program pro správu úkolů a plánování času. Uživatelé by měli moci přidávat úkoly, nastavovat priority a sledovat splnění úkolů.