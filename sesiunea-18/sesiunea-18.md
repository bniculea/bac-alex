# Sesiunea 18

## Agenda
 - Rezolvare simulare 2025

## Rezolvare varianta simulare 2025

### Subiectul I

1. Rezolvare:
    - Valoare expresie: 810
    - a - fals
    - b - fals
    - c - true
    - d - fals
    - Raspuns corect: `C`

2. Rezolvare:
    ```json
        Calculam pentru fiecare valoare:
        f(5) = 
            5 * f(55) + 5 la intoarcere
                = 5 * f(555) + 55 la intoaRCERE
                    = 5
                = 5 * 5 + 55 = 80
            = 5 * 80 + 5 = 405
        
        f(2) = 
            5 * f(25) + 2
                = 5 * f(255) + 25
                    = 5 * f(2555) +  255
                        = 5
                    = 280
                = 5*280+25 = 1425
            = 5 * 1425 + 2  = 7127
        
        f(1) =>
            5 * f(15) + 1
                = 5 * f(155) + 15
                    = 5 * f(1555) + 155
                        = 5
                    = 180
                = 915
            = 4576 => fals

        f(0) =>
            5 * f(5) + 0
                = 5 * f(55) + 5
                    = 5 * f(555) + 55
                        = 5
                    = 80
                = 405
            = 2025
    ```
    - Raspuns corect: `D`

3. Rezolvare:
    - Stim ca un element se afla pe diagonala secundara daca `i+j = n-1`
    - Din prima excludem  b si d deoarece sunt incorecte dpdv al sintaxei
    - Pentru `a` avem: 1999+25 = 2024 deci indeplineste cerinta
    - Doar de verificare la `c` AVEM 25+52 = 77 care nu e nici pe aproape de cerinta
    - Raspuns corect: `A`

4. Rezolvare:
    - Din vectorul de tati deducem urmatoarele:
        ```json
            1 2 3 4 5 6 7 8 9 10 11
            4 3 7 6 7 8 6 0 7 7  7

            Radacina: 8
            8 tata pentru: 6
            6 tata pentru: 4 si 7
            4 tata pentru: 1
            7 tata pentru: 3,5,9,10,11
            3 tata pentru: 2
            Deci rezulta arborele de mai jos:

        ```
         ![Nod 2 radacina](imagini/simulare-s1-e4.png)
        - Din poza vedem ca numarul maxim de fii este 5, si anume cei ai nodului 7
    - Raspuns corect: `B`
5. Rezolvare:
    - Din teorie stim ca un arbore (Graf conex fara cicluri) cu n noduri are exact n-1 muchii
    - Si acum daca aplicam regula pe fiecare dintre cele 5 componente avem n(i)-1 muchii:
        - n1 + n2 + n3 + n4 + n5 = 25
        - Deci numarul total de muchii este egal cu 25 -5 = 20. Cele 5 vin din faptul ca la fiecare componenta avem n - 1 si cum avem 5 componente, scadem 5
    - Raspuns corect: `A`

### Subiectul II

1. Rezolvare:
    - a
        ```json
            m = 20, n = 25
            m mai mic decat 25 deci o sa le inversam:
            n = 20, m 25
            k = 25;
            pentru i = 25
                scrie k => scrie 25 ' '
                daca i % 2 == 0 fals

                k = 24
            pentru i = 24
                scrie k => scrie 24 ' '
                daca i % 2 == 0 adevarat:
                    k = 23
                    scrie '*'
                k = 22
            pentru i = 23
                scrie k => scrie 22 ' '
                daca i % 2 == 0 false
                k = k - 1 = 21
            pentru i = 22
                scrie k => scrie 21 ' '
                daca i % 2 == 0 true
                    k = 20
                    scriew '*'
                k = `19
            pentrue i = 21
                scrie k => 19 ' ';
                daca i % 2 == 0 fals
                k = k -1 = 18
            pentru i = 20
                scriew k => scrie 18 ' '
                daca i % 2 == 0 TRUE
                    k = 17
                    scrie '*'
                k = 16
            
        ```
        - Programul afiseaza: 25 24 *22 21 *19 18 *
        - Atentie la spatieri
    - b
        ```json
            m = 5;
            Oricare dintre 3,10,11 satisfac  cerinta
            Observam ca orice ar fi, cel mai mic numar trebuie sa fie impar, pentru a evita scrierea de steluta, asta in primul rand. Si dupa aceea observam ca pentru un i par, k scade de 2 ori, asta ca sa ne facem calculul mai usor.
        ```
    - c
        ```c++
            #include <iostream>

            using namespace std;


            int main() {
                int m, n;
                cin >> m >> n;

                if (m < n) {
                    n = n+m;
                    m = n - m;
                    n = n-m;
                }

                int k = m;
                for (int i = m; i >=n; i--) {
                    cout << k << " ";
                    if (i%2 == 0) {
                        k = k -1;
                        cout << "*";
                    }
                    k = k -1;
                }
                return 0;
            }

        ```
    - d
        ```json
            citește m,n
            (numere naturale)
            ┌dacă m<n atunci
            │ n<-n+m
            │ m<-n-m
            │ n<-n-m
            └■
            k<-m
            i<-m
            ┌cat timp i >= n execută
            │ scrie k, ' '
            │┌dacă i%2=0 atunci
            ││ k<-k-1
            ││ scrie '*'
            │└■
            │ k<-k-1
            | i <- i-1
            └■
        ```

2. Rezolvare
    ```json
        Avem urmatoarele
        {20,              10,               50,               20,             150,      50,            100,         150 }
        {cască, clipsuri pentru nas, costum de înot, dopuri pentru urechi, înotătoare, ochelari, pantofi acvatici, placă}


        (cască, clipsuri pentru nas, costum de înot, dopuri pentru urechi, pantofi acvatici),
        (cască, clipsuri pentru nas, dopuri pentru urechi,înotătoare), 
        (cască, clipsuri pentru nas, dopuri pentru urechi, ochelari, pantofi acvatici)

        (cască, clipsuri pentru nas,dopuri pentru urechi,placa)
        (costum de inot, inotatoare)
    ```


3. Rezolvare
    ```c++
         #include <iostream>
        #include <cstring>
        using namespace std;
        //-----------------------------------------
        struct specialist {
            int anAngajare;
            struct {char CNP[14]; int anNastere;} personal;
        }s[30];
        //------------------------------------------

        // Nota: pentru bac ai nevoie doar de codul ce se gaseste intre liniile hasurate:
        // Mai jos este doar pentru a ne verifica
        int main() {
            int anNastereInitial = 1970;
            int anAngajareInitial = 1990;
            for (int i = 0; i < 30; i++) {
                s[i].anAngajare = anAngajareInitial+i;
                s[i].personal.anNastere = anNastereInitial+i;
                strcpy(s[i].personal.CNP, "192111111111");
            }

            cout << s[5].personal.CNP<<endl;
            cout << s[5].personal.anNastere<<endl;
            cout << s[5].anAngajare<<endl;;
            return 0;
        }
    ```

### Subiectul III

1. Rezolvare:
    ```c++
        #include <iostream>

        using namespace std;

        void harsad(int k, int& n);

        int main() {
            int n;
            harsad(2027, n);
            cout << n << endl;
            return 0;
        }

        void harsad(int k, int& n) {
            for (int i = 1; i <=k; i++) {
                int sumaCifreI = 0;
                int copieI = i;
                while (copieI > 0) {
                    sumaCifreI += copieI % 10;
                    copieI /= 10;
                }
                if (i % sumaCifreI == 0) {
                    n = i;
                }
            }
        }
    ```

2. Rezolvare:
    - Nota:
        - Intotdeauna incearca sa spargi problema in bucatele mai mici pe care stii sa le faci.
        - Deci primul pas ar fi sa incercam sa gasim toate operatiile de care avem nevoie. In cazul nostru acestea ar fi:
            - Sa determinam daca un caracter este sau nu vocala
            - Sa numaram cate vocale sunt intr-un cuvant
            - Sa determinam daca 2 cuvinte sunt sau nu asemenea
                - Aici o sa folosim logica de mai sus adica:
                    1. Verificam daca au aceleasi numar de vocale si daca sunt diferite (folosind `strcmp`)
            - Dupa aceea, pur si simplu iteram prin matricea de cuvinte si afisam cuvintele care indeplinesc conditia
    ```c++
        #include <cstring>
        #include <iostream>

        using namespace std;

        int esteVocala(char c);
        int contorVocale(char cuvant[]);
        int esteAsemenea(char cuvant1[], char cuvant2[]);

        int main() {
            int n;
            cin >> n;
            int exista = 0;
            char cuvinte[n][21];
            for (int i = 0; i < n; i++) {
                cin >> cuvinte[i];
            }

            for (int i = 0; i < n-1; i++) {
                if (esteAsemenea(cuvinte[i], cuvinte[n-1])) {
                    cout << cuvinte[i] << endl;
                    exista = 1;
                }
            }

            if (exista == 0) {
                cout << "nu exista"
            }

            return 0;
        }


        int esteAsemenea(char cuvant1[], char cuvant2[]) {
            if ( contorVocale(cuvant1) == contorVocale(cuvant2) &&
                strcmp(cuvant1, cuvant2) != 0
            ) {
                return 1;
            } else {
                return 0;
            }
        }

        int contorVocale(char cuvant[]) {
            int contor = 0;
            for (int i = 0; i < strlen(cuvant); i++) {
                if (esteVocala(cuvant[i])) {
                    contor++;
                }
            }
            return contor;
        }

        int esteVocala(char c) {
            return strchr("aeiou", c) != NULL;
        }

    ```

3. Rezolvare:
    - a
        ```json
            O sa implementam un algoritm care va folosi un vector de aparitii pentru numerele din intervalul [10,99]. Practic, citim cele doua numere care reprezinta numarul de cercei si numarul de pandantive dupa care citim mai intai linia ce contine cerceii. La fiecare cercel citit, extragem primele doua cifre si vedem daca nu cumva deja avem o aparitie pentru acest numar, caz in care oprim procesarea si afisam "DA", daca nu avem o intrare in vectorul de aparitii atunci calculam inversul numarului format din cele doua cifre, actualizam frecventa inversului si daca aceasta este mai mare ca 1 inseamna ca am gasit un set potrivit si am oprit procesarea dupa ce afisam "DA".
            Daca nu am gasit un set potrivit dupa ce am terminat de parcurs cerceii, atunci aplicam exact aceeasi procedura si pentru pandantive.
            Daca la final nu avem un set potrivit nici dupa ce am analizat pandantivele, afisam mesajul "NU". Algoritmul este eficient din punct de vedere al timpului de executie deoarece fisierul este parcurs cel mult o data insa in acelasi timp, la primul set potrivit gasit, oprim parcurgerea lui.
        ```
    - b
        ```c++
            #include <iostream>
            #include <fstream>

            using namespace std;
            int  calculeazaInvers(int numar);
            int extragePrimeleDouaCifre(int numar);
            int proceseazaNumarSiVerifica(int, int[]);

            int main() {
                ifstream fin("bijuterii.in");
                int nc, np;
                fin >> nc >> np;
                int frecventa[100] = {0};
                int exista = 0;
                for (int i = 0; i < nc; i++) {
                    int cercei;
                    fin >> cercei;
                    exista = proceseazaNumarSiVerifica(cercei, frecventa);
                    if (exista == 1) {
                        cout << "DA";
                        break;
                    }
                }

                if (exista == 0) {
                    for (int i = 0; i < np; i++) {
                        int pandantiv;
                        fin >> pandantiv;
                        exista = proceseazaNumarSiVerifica(pandantiv, frecventa);
                        if (exista == 1) {
                            cout << "DA";
                            break;
                        }
                    }
                }

                if (exista == 0) {
                    cout << "NU";
                }

                fin.close();

                return 0;
            }

            /**
            * Aceasta functie intoarce inversul unui numar.
            */
            int  calculeazaInvers(int numar) {
                int rezultat = 0;
                while (numar != 0) {
                    int ultimaCifra = numar % 10;
                    rezultat = rezultat * 10 + ultimaCifra;
                    numar = numar / 10;
                }

                return rezultat;
            }

            /**
            * Aceasta functie extrage primele doua cifre ale numarului prin impartirea succesiva
            * la 10, cat timp acesta este mai mare sau egal cu 100.
            */
            int extragePrimeleDouaCifre(int numar) {
                while (numar >= 100) {
                    numar /= 10;
                }
                return numar;
            }

            /**
            *  Aceasta functie extrage primele doua cifre dintr-un numar si verifica daca
            *  avem o intrare in vectorul de aparitii la pozitia indicata de catre numarul format
            *  din cele doua cifre, caz in care setam flag-ul exista pe 1.
            *  Daca nu exista o intrare pentru numarul format din cele 2 cifre, calculam numarul format din inversul
            *  celor doua cifre, actualizam frecventa la pozitia indicata de acest numar si din nou daca avem o valoarea
            *   mai mare decat 1, am gasit un set potrivit si setam flag-ul pe 1.
            */
            int proceseazaNumarSiVerifica(int numar, int frecventa[]) {
                int exista = 0;
                int primeleDouaCifre = extragePrimeleDouaCifre(numar);
                if (frecventa[primeleDouaCifre] > 1) {
                    frecventa[primeleDouaCifre]++;
                    exista = 1;
                } else {
                    int invers = calculeazaInvers(primeleDouaCifre);
                    frecventa[invers]++;
                    if (frecventa[primeleDouaCifre] > 1) {
                        exista = 1;
                    }
                }

                return exista;
            }
        ```


