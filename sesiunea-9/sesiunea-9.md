# Sesiunea 9

## Agenda

- Rezolvare exercitii Sesiunea 8
- Introducere in functii
- Exercitii functii
- Tema


## Rezolvare exercitii tema Sesiunea 8

1. Rezolvare
    ```c++
        #include <iostream>
        #include <fstream>

        using namespace std;

        int main(){
            int n;
            cin >> n;
            float matrice[n][n];
            float blurat[n][n];
            for (int i = 0; i < n; i++) {
                for (int j = 0; j < n; j++) {
                    cin >> matrice[i][j];
                }
            }
            for (int i = 0; i < n; i++) {
                for (int j = 0; j < n; j++) {
                    float medieVecini =0.0;

                    float vecinNord = matrice[i-1][j];
                    float vecinSud = matrice[i+1][j];
                    float vecinVest = matrice[i][j-1];
                    float vecinEst = matrice[i][j+1];
                    if (i == 0) {
                        if (j == 0) {
                            medieVecini = (vecinEst + vecinSud) / 2;
                        } else if (j == n - 1) {
                            medieVecini = (vecinVest + vecinSud) / 2;
                        } else {
                            medieVecini = (vecinVest + vecinEst + vecinSud) / 3;
                        }
                    } else if (i == n - 1) {
                        if (j == 0) {
                            medieVecini = (vecinNord + vecinEst) / 2;
                        } else if (j == n - 1) {
                            medieVecini = (vecinNord + vecinVest) / 2;
                        } else {
                            medieVecini = (vecinNord + vecinVest + vecinEst) / 3;
                        }
                    } else {
                        if (j == 0) {
                            medieVecini = (vecinNord + vecinSud + vecinEst) / 3;
                        } else if (j == n - 1) {
                            medieVecini = (vecinNord + vecinSud + vecinVest) / 3;
                        } else {
                            medieVecini = (vecinEst + vecinSud + vecinVest + vecinNord) / 4;
                        }
                    }

                    blurat[i][j] = medieVecini;
                }
            }

            for (int i = 0; i < n; i++) {
                for (int j = 0; j < n; j++) {
                    cout << blurat[i][j] << " ";
                }
                cout << endl;
            }

            return 0;
        }
    ```

2. Rezolvare:
    ```c++
        #include <iostream>
        #include <fstream>

        using namespace std;

        int main(){
            int n;
            cin >> n;
            int matrice[n][n];
            for (int i = 0; i < n; i++) {
                for (int j = 0; j < n; j++) {
                    cin >> matrice[i][j];
                }
            }
            int sumaZonaNord = 0, sumaZonaEst = 0, sumaZonaSud = 0, sumaZonaVest = 0;
            for (int i = 0; i < n; i++) {
                for (int j = 0; j < n; j++) {
                    if (j > i && i+j < n - 1) {
                        sumaZonaNord += matrice[i][j];
                    } else if (j > i && i + j > n - 1 ) {
                        sumaZonaEst += matrice[i][j];
                    } else if (i > j && i + j > n - 1) {
                        sumaZonaSud += matrice[i][j];
                    } else if (i > j && i+j < n-1) {
                        sumaZonaVest += matrice[i][j];
                    }
                }
            }

            int sumaEV = sumaZonaEst + sumaZonaVest;
            int sumaNS = sumaZonaSud + sumaZonaNord;

            if (sumaEV > sumaNS) {
                cout << sumaEV - sumaNS << endl;
            } else {
                cout << sumaNS - sumaEV << endl;
            }


            return 0;
        }
    ```

3. Rezolvare:
    ```c++
            #include <iostream>

            using namespace std;
            /**
            * Observam ca pe diagonala principala avem multiplii lui k pe care ii putem calcula astfel:
            * matrice[i][j] = k * (i+1). Folosim i+1 deoarece pornim de la 0 cu indicele.
            * Dupa care observam ca pentru fiecare element din dreapta diagonalei principale, scadem din valoarea
            * de pe diagonala principala, distanta dintre elementul curent si diagonala principala, lucru pe care
            * il aflam cu j - i
            *
            * Iar pentru elementele din stanga diagonalei principale, adunam la diagonala principala distanta dintre
            * elementul curent si diagonala principala, lucru pe care il aflam cu i - j.
            */

            int main() {
                int k,n;
                cin >> k >> n;
                int matrice[n][n];
                for (int i = 0; i < n; i++) {
                    for (int j = 0; j < n; j++) {
                        int valoareDiagonalaPrincipala = k * (i+1);
                        if (i == j) {
                            matrice[i][j] = valoareDiagonalaPrincipala;
                        } else if (j > i) {
                            matrice[i][j] = valoareDiagonalaPrincipala - (j-i);
                        } else {
                            matrice[i][j] = valoareDiagonalaPrincipala + (i - j);
                        }
                    }
                }

                for (int i = 0; i < n; i++) {
                    for (int j = 0; j < n; j++) {
                        cout << matrice[i][j] << " ";
                    }
                    cout << endl;
                }

                return 0;

            }
    ```

4. Rezolvare:
    ```c++
        #include <iostream>

        using namespace std;

        int main() {
            int i, j;
            int a[9][9];
            // Pentru bac trebuie sa scrii doar ce este intre liniile hasurate
            //-----------------------------------------
            for(i = 0; i < 9; i++) {
                for (j = 0; j< 9; j++) {
                    if (i +j <= 3 || i+j >= 13 ) {
                        a[i][j] = 4;
                    } else {
                        a[i][j] = 2;
                    }
                }
            }
            //------------------------------------------

            for(i = 0; i < 9; i++) {
                for (j = 0; j< 9; j++) {
                    cout << a[i][j] << " ";
                }
                cout << endl;
            }
            return 0;
        }

    ```

## Introducere in functii / subprograme
- O funcție definește o anumită sarcină pe care dorim să o îndeplinim, cum ar fi:
    - calcularea pătratului unui număr-
    - afișarea unui mesaj gen: "Hello world"
    - afișarea numelui complet al unei persoane
    - etc.
- Daca luam de exemplu o functie care calculeaza media geometrica a 3 numere:
    - Te poti gandi ca in loc sa copiezi undeva la 4,5 linii de cod de fiecare data, o sa ai doar o linie de cod.
    - O sa fie ceva gen: `calculeazaMedie(x,y,z)` sau `calculeazaMedie(a,b,c)`
    - daca nu ai fi avut functii, trebuie sa copiezi peste tot, toata logica ce iti calcula media.
- Un avantaj mare al functiilor este ca daca avem o problema de logica in calculul/operatiile pe care il/le face functia noastra (si prespunem ca e chemata in muuuulte locuri) noi vom avea de corectat intr-un singur loc, anume unde am definit functia si solutia probleme se va propaga automat peste tot unde e folosita.

- Pentru definirea unei funcții, vom utiliza următorul șablon:
    ```c++
        <tip întoarcere> <nume funcție> (<listă de parametri>){
        <corpul funcției>
    }
    ```
    - exemplu cu functie care intoarce o valoare:
        ```c++
            int computeAverage(int x, int y) {
                int average = ( x + y ) / 2;

                return average;
            }
        ```
     - exemplu cu functie care nu intoarce o valoare:
        ```c++
            void displayAverage(int x, int y) {
                int average = ( x + y ) / 2;

                cout << "Media celor doua numere este: " << average;
            }
        ```
- Acum, sa disecam fiecare parte din sablonul functiei:
- `<tip întoarcere>` 
    - O funcție poate întoarce una sau zero valori.
    - Daca intoarce o valoare aceasta poate fi de tipul `int`, `float`, `double`, etc.
    - Dacă nu întoarce o valoare, ar trebui să folosim cuvântul cheie `void` înainte de a declara numele funcției.

- `<nume funcție>` 
    - reprezintă numele pe care îl dăm acelei bucăți de cod care gestionează o sarcină specifică pentru noi. Acest lucru este util atunci când dorim să apelăm funcția ulterior.
        - Apelul unei funcții este ca o scurtătură, dorim doar să aducem funcționalitatea implementata in functie, pentru a o folosi în logica noastră, fără a o recrea.
            - De multe ori, functiile pe care le folosim, nici nu sunt scrise de noi. De exemplu, folosim funcția `cout`, dar aceasta este o bucată de cod care nu a fost creată de noi.
- `<listă de parametri>` 
    - reprezintă datele de intrare folosite de funcția noastră pentru a-și îndeplini responsabilitățile.
    - Putem extrapola putin si sa vedem functia ca pe o reteta de prajituri
        - `parametrii` sunt ingredientele pentru rețeta noastră (de exemplu, zahăr, lapte, etc.)
        - rețeta este logica care amestecă ingredientele (a.k.a. parametrii)
        - prajitura va fi rezultatul final al funcției noastre atunci când este apelată.

Nota: 
- Cu excepția funcției principale (adica `main`), fiecare funcție trebuie să fie definită înainte de a fi folosită.
Atunci când definim o funcție, trebuie doar să specificăm tipul întoarcerii, numele și lista de parametri, de exemplu:
    - `void afișareAdresă();`
    - `int calculDistanță(int x, int y);`
- De retinut ca o functie poate sa cheme o alta functie (sau mai multe). A se vedea exercitiul `6`.

### Exemple functii
1. Scrieti o functie care transforma secundele, primite ca si parametru, in ore, minute si secunde, dupa care afisaza rezultatul in formatul: `HH:MM:SS`.
- Solutie:
    ```c++
        #include <iostream>
        using namespace std;

        void convertesteSecunde(int secunde);

        int main() {
            int secunde;
            cout << "Introduceti numarul total de secunde: ";
            cin >> secunde;
            convertSecondsToFriendlyFormat(secunde);

            return 0;
        }

        void convertesteSecunde(int secunde) {
            int ore = secunde / 3600;
            int minute = (secunde % 3600) / 60;
            int secundeRamase = secunde - (ore * 3600) - (minute * 60);

            cout << ore<<":"<<minute<<":"<<secundeRamase;
        }
    ```
2. Scrieti o functie care primeste ca si parametru un numar natural `n`. unde `n` > 100 si `n` <= 99999. Functia va returna cate cifre ale numarului sunt impare, -1 in cazul in care niciuna nu indeplineste conditia.
-  Date de intrare: `n` = 123456
-  Date de iesire: 3
-  Date de intrare: `n` = 2468
-  Date de iesire: -1
-  Solutie:
    ```c++
    #include <iostream>
    using namespace std;

    int numaraImpare(int n);

    int main() {
        int n;
        cout << "Introduceti n: ";
        cin >> n;
        cout << numaraImpare(n);

        return 0;
    }

    int numaraImpare(int n) {
        int contor = 0;
        while (n > 0) {
            int ultimaCifra = n % 10;
            if (ultimaCifra % 2 != 0) {
                contor++;
            }
            n = n / 10;
        }
        if (contor == 0) {
            return -1;
        } else {
            return contor;
        }
    }
    ```

3. Subprogramul `DoiTrei` are un parametru, `n`, prin care primeste un numar natural (n apartine intervalului [0, 10^9]). Subprogramul returneaza valoarea 1 daca toate cifrele lui `n` sunt din multimea `{2,3}` sau valoarea 0 in caz contrar. Scrieti definitia completa a programului.
- Date de intrare: `n` = 22323
- Date de iesire: 1
- Date de intrare: `n` = 2023
- Date de iesire: 0
- Solutie:
    ```c++
    #include <iostream>
    using namespace std;

    int DoiTrei(int n);

    int main() {
        int n;
        cout << "Introduceti n: ";
        cin >> n;
        cout << DoiTrei(n);

        return 0;
    }

    int DoiTrei(int n) {
        int rezultat = 1;
        while (n > 0) {
            int ultimaCifra = n % 10;
            if (ultimaCifra != 2 && ultimaCifra != 3) {
                rezultat = 0;
                break;
            }

            n = n / 10;
        }

        return rezultat;
    }
    ```

4. Scrieti un program care sa contina un subprogram ce va primi ca si parametru un numar `n`. Subprogramul va afisa toti divizorii numarului, separati prin spatiu.
- Date de intrare: `n` = 15
- Date de iesire: 1,3,5,15
- Solutie:
    ```c++
    #include <iostream>
    using namespace std;

    void afiseazaDivizori(int n);
    int main() {
        int n;
        cout << "Introduceti n: ";
        cin >> n;
        afiseazaDivizori(n);

        return 0;
    }

    void afiseazaDivizori(int n) {
        for (int i = 1; i <= n; i++) {
            if ( n % i == 0) {
                cout << i << " ";
            }
        }
    }
    ```

5. Scrieti un program care sa contina un subprogram ce va primi ca si parametru un numar `n`. Subprogramul va returna `1` daca numarul este `prim` sau `0` in caz contrar.
- Date de intrare: `n` = 21
- Date de iesire: 0
- Date de intrare: `n` = 13
- Date de iesire: 1
- Solutie: 
    ```c++
        #include <iostream>
        using namespace std;

        int estePrim(int n);

        int main() {
            int n;
            cout << "Introduceti n: ";
            cin >> n;
            cout << estePrim(n);

            return 0;
        }

        int estePrim(int n) {
            int rezultat = 1;
            for (int i = 2; i < n/2; i++) {
                if (n % i == 0) {
                    rezultat = 0;
                    break;
                }
            }

            return rezultat;
        }
    ```

6. Scrieti un program C++ care citeste de la tastatura un sir de caractere de maximum 50 de caractere. Programul va numara cate consoane si cate vocale sunt in sir. Atentie la faptul ca sirul de caractere poate contine caractere alfanumerice si literele vor fi toate litere mici ale alfabetului.
- Date de intrare: "ana are ac cu ata de 2 metri."
- Date de iesire:
    - `Consoane: 9`: 
    - `Vocale: 11`
- Solutie:
    ```c++
        #include <iostream>
        #include <string.h>

        using namespace std;

        int esteVocala(char ch);
        int esteConsoana(char ch);

        int main() {
        char propozitie[50];
        cout << "Introduceti maximum 50 de caractere de la tastatura: ";
        cin.getline(propozitie, 50);

        int totalConsoane = 0;
        int totalVocale = 0;
        for (int i = 0; i < strlen(propozitie); i ++) {
            if (esteVocala(propozitie[i]) == 1) {
                totalVocale++;
            } else if (esteConsoana(propozitie[i])) {
                totalConsoane++;
            }
        }

        cout << "Consoane: " << totalConsoane << endl;
        cout << "Vocale: " << totalVocale;

            return 0;
        }

        int esteVocala(char ch) {
            return strchr("aeiou", ch) != nullptr;
        }

        int esteConsoana(char ch) {
            if (ch >= 'a' && ch <= 'z' && !esteVocala(ch)){
                return 1;
            } else {
                return 0;
            }
        }
    ```
## Exercitii functii / subprogramae