# java_beginner 

**************************************************************************************************
1. While Schleife 

// Möglichkeit I:

public class Main {
    public static void main(String[] args) {
        int number = 1;

      while (number <= 10) {
          System.out.println("Die Nummern: " + number);
          number++;
      }
    }
 }


// Möglichkeit II:

public class Main {
    public static void main(String[] args) {
        int number = 1;
        boolean cont = true;

      while (cont) {
          System.out.println("Die Nummern: " + number);
          number++;
          if (number == 10) {
              cont = false;    // alternativ kann man "break;" verwenden
          }
      }
    }
}


// Möglichkeit III: 

public class Main {
    public static void main(String[] args) {
        int number = 1;

      while (true) {
          System.out.println("Die Nummern: " + number);
          number++;
          if (number > 10) {
              break;
          }
      }
    }
}


// Möglichkeit IV:

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner wahl = new Scanner(System.in);
        int wieder = 1;

      while (wieder == 1) {
          System.out.println("hier ist das zu wiederholende Objekt ");
          System.out.println("Möchtest du wiederholen? für ja bitte 1 drüken.");
          wieder = wahl.nextInt();
      }
      System.out.println("Beendet");
    }
}

***********************************************************************************************************
2. For Schleife 

public class Main {
    public static void main(String[] args) {
        for (int i = 0; i < 10; i+=2) {
            System.out.println("Zahl - " + i);
        }
    }
}


// While Schleife:

public class Main {
    public static void main(String[] args) {
    
        int zahl = 1;

        while(zahl <=10){
            System.out.println(zahl);
            zahl++; 
        }
    }
}



// Do-While Schlaife:

public class Main {
    public static void main(String[] args) {
        int zahl = 1;

        do {                            // erst einmal durchführung dann die Bedingung achten
            System.out.println(zahl);
            zahl++;
        }
        while(zahl <= 10); 
    }
}


// Verschachtelte Schleifen:

public class Main {
    public static void main(String[] args) {

        for (int i = 0; i < 4; i++) {
            for (int j = 0; j < 6; j++) {
                System.out.print(j);
            }
            System.out.println();
        }
    }
}

************************************************************************************************************
3. Random Klasse 

import java.util.Random;

public class Main {
    public static void main(String[] args) {
      Random myRandom = new Random();               // generiert die Zufallszahlen
      int zufallszahl = myRandom.nextInt();
      System.out.println(zufallszahl);
    }
}

*******************************************************************************************************************
4. Array:

import java.sql.Array;

public class Main {
    public static void main(String[] args) {

       String[] myArray = new String[3];     // max. 3 Inhalte erlaubt

       myArray[0] = "AAA";
       myArray[1] = "BBB";
       myArray[2] = "CCC";

       for (int i = 0; i < myArray.length; i++) {
           System.out.println(myArray[i]);
       }
    }
}

******************************************************************************************
5. Array Möglichkeit 2: 

public class Main {
    public static void main(String[] args) {

       String[] myArray = {"AAA", "BBB", "CCC"};

       for (int i = 0; i < myArray.length; i++) {
           System.out.println(myArray[i]);
       }
    }
}

*********************************************************************************
6. Foreach Schleife: 

public class Main {
    public static void main(String[] args) {

       String[] myArray = {"AAA", "BBB", "CCC"};

       for (String inhalt : myArray) {          //durchlaufe in Array "myArray" und speichere die Inhalte in Typ "inhalt"
           System.out.println(inhalt);
       }
    }
}

*****************************************************************************************
7. Mehrdimensionale Arrays : ***********************************************************

public class Main {
    public static void main(String[] args) {

       String[][] Lagerplatz = new String[3][2];   //3 va 2 lar 1 dan boshlab hisoblanadi 

        Lagerplatz[0][0] = "A1";
        Lagerplatz[0][1] = "A2";

        Lagerplatz[1][0] = "B1";
        Lagerplatz[1][1] = "B2";

        Lagerplatz[2][0] = "C1";
        Lagerplatz[2][1] = "C2";

       for (int i = 0; i < Lagerplatz.length; i++) {
           for (int j = 0; j < Lagerplatz[i].length; j++) {
            System.out.print(Lagerplatz[i][j] + " ");
           }
           System.out.println();
       }
    }
}

***************************************************************************************************
8. Methoden: *************************************************************************************

public class Main {
    public static void main(String[] args) {

        System.out.println("Hiert kommt ein Method:");

        myMethod();
    }
    public static void myMethod() {        // void bedeutet kein Rückgabewert 
        int a = 5;
        int b = 10;
        System.out.println(a + b);
    }
}

****************************************************************************************************
9. Methode mit Pareameter **************************************************************************

public class Main {
    public static void main(String[] args) {

        System.out.println("Hiert kommt ein Method:");

        myMethod(2, 5);
    }
    public static void myMethod(int parameter1, int parameter2) {
        int a = parameter1;
        int b = parameter2;
        System.out.println(a + b);
    }
}

********************************************************************************************************
10. Methode mit Rückgabewert ****************************************************************************

public class Main {
    public static void main(String[] args) {

        System.out.println("Hiert kommt ein Method:");

        myMethod(2, 5);     //Ergebnis der Methode ist hier gespeichert, zeigt aber nicht
        System.out.println(myMethod(2, 5));    
    }
    public static int myMethod(int parameter1, int parameter2) {
        int a = parameter1 + parameter2;
        return a;
    }
}

***********************************************************************************************************
11.  Objekt Orientierte Programmierung(OOP)
    // Klasse - Bauplan für Objekte 
    // Attribute - Eigenschaften der Objekte 
    // Methoden -  Funktionen der Objekte 
    
    
   //Hier ist Main Klasse: 
    
    public class Main {
    public static void main(String[] args) {

        Katze katzeObjekt = new Katze();

        katzeObjekt.miau();

        katzeObjekt.rechnen(10, 8);

    }

}

// Hier ist die Klasse Katze: 

public class Katze {

    //Attribute:
    int alter;
    String farbe;
    String rasse;
    boolean springen;

    //Methoden:
    public void miau() {
        System.out.println("Miauuuuu!!!");
    }

    public void rechnen(int zahl1, int zahl2) {
        System.out.println(zahl1 + zahl2);
    }

}

***************************************************************************************************************
12. Parameter übergeben:

// Main Klass (Hauptklasse): ------------------------------------------------------------------
public class Main {
    public static void main(String[] args) {
        
        //Attribute werden initialisiert: 
        Katze katzeObjekt = new Katze();
        katzeObjekt.alter = 3;
        katzeObjekt.farbe = "gelb";
        katzeObjekt.rasse = "heimisch";
        katzeObjekt.springen = true;

        katzeObjekt.test(true, "Miiiiiia!!!");


    }

}

// Klasse Katze: ----------------------------------------------------------------------------------------

public class Katze {

    //Attribute:
    int alter;
    String farbe;
    String rasse;
    boolean springen;

    //Methoden:
    public void miau(String machMiau) {     // miau Methode hat Parameter machMiau, hier übernimmt das Parameter machMiau den Parameter_2
        System.out.println(machMiau);
    }

    public void test(boolean Parameter_1, String Parameter_2) {      // test Methode hat 2 Parametern.
        if (Parameter_1) {                      //wenn Parameter_1 true ist, dann führe das Method miau.
            miau(Parameter_2);                  //miau übernimmt das Parameter_2.
        }
    }

}

********************************************************************************************************************************************
13. Konstruktor:

// Konstruktor dient die Attribute einfach zu initialisieren.


public class Main {
    public static void main(String[] args) {

        Katze katzeObjekt = new Katze(2, "gelb", "heimisch", true);
        System.out.println("katzeObjekt ist " + katzeObjekt.alter + " jahre alt");
    }
}

----------------------------------------------------------------------------------------------------------------------------
public class Katze {

    //Attribute:
    int alter;
    String farbe;
    String rasse;
    boolean springen;

    //Konstruktor:
    public Katze(int alter, String farbe, String rasse, boolean springen) {     //hier sind die Parametern mit gleichen Namen wie Attribute
        this.alter = alter;   //this bedeutet Attribute alter. Also Attribut this.alter übernimmt den Parameter alter.
        this.farbe = farbe;
        this.rasse = rasse;
        this.springen = springen;
    }
}

****************************************************************************************************************************
// Konstruktor.

public class Main {
    public static void main(String[] args) {

        Katze katzeObjekt = new Katze(2, "gelb", "heimisch", true);
        System.out.println("katzeObjekt ist " + katzeObjekt.alter + " jahre alt.");

        Katze mashka = new Katze(0.2, "schwarz", "unbekannt", true);
        System.out.print("Mashka ist " + mashka.alter + " Jahre alt, " + mashka.farbe + ", Rasse ist " + mashka.rasse + ", und kann ");
        if (mashka.springen) {
            System.out.print("springen.");
        } else {
            System.out.print("nicht springen, weil er noch jung ist.");
        }
    }
}

----------------------------------------------------------------------------------------------------------

public class Katze {

    //Attribute:
    double alter;
    String farbe;
    String rasse;
    boolean springen;
    
    //Konstruktor:
    public Katze(double alter, String farbe, String rasse, boolean springen) {     //hier sind die Parametern mit gleichen Namen wie Attribute
        this.alter = alter;   //this bedeutet Attribute alter. Also Attribut this.alter übernimmt den Parameter alter.
        this.farbe = farbe;
        this.rasse = rasse;
        this.springen = springen;
    }
}


***********************************************************************************************************************
14. Rückgabewert--------------------------------------------------------------------------------


public class Main {

    public static void main(String[] args) {        //void bedeutet, dass diese Methode kein Rückgabewert zurückgibt. 
        int summe = addition(5, 10);
        System.out.println(summe);
    }

    public static int addition(int zahl1, int zahl2) {     //ohne void gibt Methode einen Rückgabewert zurück.
        return zahl1 + zahl2;
    }
}



Rückgabewert -------------------------------------------------------------------------------------------------------------


public class Main {
    public static void main(String[] args) {
        Katze katze1 = fremdKatze(1);
    }

    public static Katze fremdKatze(int alter) {
        return new Katze(alter, "weiss", "qaymoq", true);
    }
}



-------------------------------------------------------------------------------------------------------------


public class Katze {
    //Attribute:
    double alter;
    String farbe;
    String rasse;
    boolean springen;

    //Konstruktor:
    public Katze(double alter, String farbe, String rasse, boolean springen) {     //hier sind die Parametern mit gleichen Namen wie Attribute
        this.alter = alter;   //this bedeutet Attribute alter. Also Attribut this.alter übernimmt den Parameter alter.
        this.farbe = farbe;
        this.rasse = rasse;
        this.springen = springen;
    }
}


**************************************************************************************************************
15. Überladung--------------------------------------------------------------------------------
     // mehrere Methoden mit gleicher Name, unterschiedlicher Parametern 



public class Main {
    public static void main(String[] args) {
        Kunde kunde1 = new Kunde("Xolid", "abc", 24, "Berlin");
        Kunde kunde2 = new Kunde("Sara", "sara1234"); 
    }
}


------------------------------------------------------------------------------------------------------------


public class Kunde {

    String name;
    String email;
    int age;
    String ort;

    public Kunde(String name, String email, int age, String ort) {
        this.name = name;
        this.email = email;
        this.age = age;
        this.ort = ort;
    }

    public Kunde(String name, String email) {
        this.name = name;
        this.email = email;
        this.age = 0;
        this.ort = "";
    }
}


*************************************************************************************************************

15. Public = offentlich, Private = nicht offentlich


public class Main {
    public static void main(String[] args) {
       Kunde kunde1 = new Kunde("Xolid", "abc", 24, "Berlin");
       kunde1.muster();
    }
}


--------------------------------------------------------------------------------------------------


public class Kunde {

    String name;
    String email;
    private int ageDiskret;     //wenn man hier private eingibt, wird es in andere Klasse nicht veröffentlicht 
    String ort;

    public Kunde(String name, String email, int ageDiskret, String ort) {
        this.name = name;
        this.email = email;
        this.ageDiskret = ageDiskret;
        this.ort = ort;
    }

    public void muster() {
        System.out.println("Halloooooo");
    }
}


**************************************************************************************************************************
16. Getter


public class Main {
    public static void main(String[] args) {
       Kunde kunde1 = new Kunde("Xolid", "abc", 24, "Berlin");
       System.out.println(kunde1.getAge());     //oldiga get desa ham boladi
       System.out.println(kunde1.shuOrt());     //oldiga get qoymasa, umuman boshqacha nomlasa boladi
    }
}


----------------------------------------------------------------------------------------------------------------------

public class Kunde {

    private String name;
    private String email;
    private int age;
    private String ort;

    public Kunde(String name, String email, int age, String ort) {
        this.name = name;
        this.email = email;
        this.age = age;
        this.ort = ort;
    }

    public int getAge() {
        return age;
    }

    public String shuOrt() {
        return ort;
    }
}


***********************************************************************************************************************
17. Setter 


public class Main {
    public static void main(String[] args) {
       Kunde kunde1 = new Kunde("Xolid", "abc", 24, "Berlin");
       kunde1.setAge(25);       //set bu yerda yoshini o'zgartiradi 
       System.out.println(kunde1.getAge());

    }
}
    
   
-----------------------------------------------------------------------------------------------------------


public class Kunde {

    private String name;
    private String email;
    private int age;
    private String ort;
    //Konstruktor
    public Kunde(String name, String email, int age, String ort) {
        this.name = name;
        this.email = email;
        this.age = age;
        this.ort = ort;
    }
    public void setAge(int newAge) {
        this.age = newAge;
    }
    public int getAge() {
        return age;
    }
}


**************************************************************************************************************

18. Static = bedeutet Objektunabhängigkeit. Sie sind unabhängig von Objekten füreinander offentlich. 


public class Main {
   static String gruß = "Hallooooo!";           

    public static void main(String[] args) {
        Kunde.bestellen();          //wegen static ist hier offentlich 
     System.out.println(gruß);      //wegen static ist hier offentlich 

    }
}


----------------------------------------------------------------------------------------------------------


public class Kunde {

    private int age = 32;
    private String ort = "Stuttgart";

    public static void bestellen() {
        System.out.println("bestellt.");
    }
}


*******************************************************************************************

19. Vererbung.

public class Main {
    
    public static void main(String[] args) {

        Motorrad motorrad1 = new Motorrad();
        motorrad1.fahren();
        System.out.println(motorrad1.preis);
    }
}


------------------------------------------------------------------------------------------------

public class Fahrrad {
    int preis = 500;

    public void fahren() {
        System.out.println("Fahrrad faehrt...");
    }
}

------------------------------------------------------------------------------------------

public class Motorrad extends Fahrrad{   //erbt von Fahrrad

}


*********************************************************************************************************************

20. Konstruktoren für Fortgeschrittene.


public class Main {

    public static void main(String[] args) {
    
        //so viele Parametern mussen sein, wie in der Konstruktion
        
        Fahrrad bike1 = new Fahrrad(22, "hec", 15, true);
        Fahrrad bike2 = new Fahrrad(44,"ndn");
        Fahrrad bike3 = new Fahrrad();
    }
}
    
    --------------------------------------------------------------------------------------------------------------------
    
    
public class Fahrrad {
    int preis;
    String marke;
    int grosse;
    boolean elektrish;

    public Fahrrad(int preis, String marke, int grosse, boolean elektrish) {    //4 Parameter
        this.preis = preis;
        this.marke = marke;
        this.grosse = grosse;
        this.elektrish = elektrish;
    }

    public Fahrrad(int preis, String marke) {     //2 Argumenten 
        this.preis = preis;
        this.marke = marke;
    }

    public Fahrrad() {        // keine Parameter, leere Konstruktor
    }
}


***********************************************************************************************************************
21. Konstruktor für Fortgeschrittene.


public class Main {

    public static void main(String[] args) {
        
        Fahrrad bike1 = new Fahrrad(700, "Baliq", "grau", "Sara");      //aus Konstruktor mit vollständigen Argumenten 
        Fahrrad bike2 = new Fahrrad(1500, "Hava");                      //aus Konstruktor mit 2 Argumenten
    }
}

----------------------------------------------------------------------------------------------------------------------------

public class Fahrrad {
    int preis;
    String marke;
    String farbe;
    String nameBesitzer;

    //Konstruktor mit vollständigen Argumenten.
    public Fahrrad(int preis, String marke, String farbe, String nameBesitzer) {
        this.preis = preis;
        this.marke = marke;
        this.farbe = farbe;
        this.nameBesitzer = nameBesitzer;
    }
    //Neue Konstruktor mit 2 Argumenten.
    public Fahrrad(int preis, String marke) {
        this.preis = preis;
        this.marke = marke;
        this.farbe = "";        //wenn das Attribut leer steht, wird es nicht berücksichtigt
        this.nameBesitzer = "";
        System.out.println("jajajaja");
    }
}


***************************************************************************************************************
22. Konstruktor mit super(). 


public class Main {

    public static void main(String[] args) {
        //Pflanzen hat von der Lebewesen geerbt. 
       Pflanzen pflanzen = new Pflanzen(44, 3.4, false);
        System.out.println(pflanzen.alter);
    }
}

-----------------------------------------------------------------------------------------------------------------

public class Lebewesen {
    int alter;
    double größe;

    public Lebewesen(int alter, double größe) {
        this.alter = alter;
        this.größe = größe;
        System.out.println("Lebewesen Konstruktor ...");
    }

}

---------------------------------------------------------------------------------------------------------------

public class Pflanzen extends Lebewesen {
    boolean hatNadel;

    public Pflanzen(int alter, double größe, boolean hatNadel) {
       super(alter, größe);     //mithilfe super() übernimmt die Parametern aus der Klasse Lebewesen.
        this.hatNadel = hatNadel;
        System.out.println("Pflanzen Konstruktor.....");
    }
}

******************************************************************************************************************

23. Überschreibung.


public class Main {

    public static void main(String[] args) {
       
        Fahrrad bike1 = new Motorrad();
        bike1.fahren();                     //Zeigt Methode aus der Motorrad 
    }
}

******************************************************************************************************
public class Fahrrad {
    String marke;
    int preis;
    String farbe;

    public void fahren() {
        System.out.println("Fahrrad fährt...");
    }
}

*****************************************************************************************************
public class Motorrad extends Fahrrad{

    public void fahren() {      //Methode muss gleiche Name und Parameter haben, wie der Klasse Fahrrad
        System.out.println("Motorrad fährt...");
    }
}

***********************************************************************************************************
24. Überladen. überladen bedeutet das, dass wir mindestens zwei Methoden vom gleichem Namen innerhalb einer Klasse haben.


    public class Main {

    public static void main(String[] args) {
        Student fleißig = new Student();

        fleißig.lernen("Mate");     
        fleißig.lernen("Chemie", "Statistik", "Thulb");
    }
}

-------------------------------------------------------------------------------------------------------

public class Student {
    String Buch;
    String Vorlesung;
    String Bibliothek;

    public void lernen(String Buch) {
        System.out.println("im Buch lernen...");
    }

    public void lernen(String Buch, String Vorlesung, String Bibliothek) {
        System.out.println("Alles lernen...");
    }
}

*********************************************************************************************************
25. Methoden Überschreiben mit super().

public class Main {

    public static void main(String[] args) {
        Motorrad motorrad1 = new Motorrad();
        motorrad1.fahren();

        System.out.println(motorrad1.preis);
    }
    
------------------------------------------------------------------------------------------------------------

public class Fahrrad {
    int preis = 500;

    public void fahren() {
        System.out.println("Fahrrad faehrt...");
    }
}

---------------------------------------------------------------------------------------------------
public class Motorrad extends Fahrrad{

    int preis = 12000;
    public void fahren() {      //Methode muss gleiche Name und Parameter haben, wie der Klasse Fahrrad
        super.fahren();      //super übernimmt das fahren() Methode aus der Klasse Fahrrad.
        System.out.println("Motorrad faehrt...");
    }
}

******************************************************************************************************

26. 
