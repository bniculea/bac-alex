# Sesiunea 14

## Agenda

- Rezolvare Varianta de rezerva pentru Iunie 2025
- Rezolvare Varianta August 2025

## Rezolvare Varianta de rezerva pentru Iunie 2025

- Link: https://www.pbinfo.ro/resurse/9dc152/examene/2025/E_d_Informatica_2025_sp_MI_C_var_07_LRO.pdf

### Subiectul I
1. Rezolvare:
    - Expresia alaturata are valoarea:
        - 7.7 + 7 = 14.7
        - Atentie la faptul ca pentru prima operatie avem un operand de tip real (float) si unul de tip intreg (int) rezultatul va fi de tipul real (float) iar pentru a doua operatie, ambii operanzi sunt intregi.
    - a => Fals
    - b => Adevaratt
    - c => Fals
    - d => Fals
    - Raspuns corect: `b`
2. Rezolvare:
    - a => sintaxa gresita. Numele atributului este `expira`, `data` este tipul atributului.
    - b => sintaxa gresita, variabila prin care accesam membrii este `m`
    - c => corect dpdv sintactic si respecta si enuntul
    - d => sintaxa gresita. Nu exista nici o proprietate in `medicament` care sa se numeasca `an` sau `luna`
    - Raspuns corect: `c`
    
3. Rezolvare:
    ```json
        Notam multimea astfel:
        {   0        1       2      3       4       5    }
        {balerini, botine, cizme, ghete, sandale, teniși }

        Stim ca nu avem voie in aceeasi comanda:
        (ghete, cizme) sau (balerini, sandale)
        adica
        (3,2) sau (0,4)


        Primele 4 solutii sunt: 
        (balerini, botine, cizme),
        (balerini, botine,ghete),
        (balerini, botine, teniși),
        (balerini, cizme, teniși)

        Adica:
        (0,1,2),
        (0,1,3),
        (0,1,5),
        (0,2,5)

        Inainte de solutia
        (cizme, sandale, tenisi)
        (2,4,5)

        
        Avem:
        (1,4,5)
        (botine, sandale, teniși)


    ```
    - Raspuns corect: `d`
4. Rezolvare:
    - Mai jos avem graful obtinut din muchiile prezentate in enunt
    ![Graf initial](imagini/s1-e4.png)
    - Acum o sa desenam pentru fiecare nod, cum arata arborele daca nodul ales ar fi radacina:
    * Daca avem nodul 1 ca si radacina avem arborele de mai jos:
    ![Nod 1 radacina](imagini/s1-e4-nod1.png)
    * Daca avem nodul 2 ca si radacina avem arborele de mai jos:
    ![Nod 2 radacina](imagini/s1-e4-nod2.png)
    * Daca avem nodul 3 ca si radacina avem arborele de mai jos:
    ![Nod 3 radacina](imagini/s1-e4-nod3.png)
    * Daca avem nodul 4 ca si radacina avem arborele de mai jos:
    ![Nod 4 radacina](imagini/s1-e4-nod4.png)
    * Daca avem nodul 5 ca si radacina avem arborele de mai jos:
    ![Nod 5 radacina](imagini/s1-e4-nod5.png)
    * Daca avem nodul 6 ca si radacina avem arborele de mai jos:
    ![Nod 6 radacina](imagini/s1-e4-nod6.png)
- Observam ca doar in cazurile cand nodurile 3,4,5,6 sunt radacini avem exact 3 frunze.
- Raspuns corect: `d`

5. Rezolvare:
    - Din enunt avem graful de mai jos:
    ![Graf cf enunt](imagini/s1-e5.png)
    - Componenta tare conexa: Graful se numește tare conex dacă între oricare două noduri distincte există cel puțin un drum.
    -  Daca adaugam muchia:
        - [3,2]
        - Obtinem graful de mai jos cu 2 componente tare conexe
        - Nota: o componenta formata dintr-un nod poate fi vazuta ca o componenta tare conexa
        ![Solutie](imagini/s1-e5-solutie.png)
    - Raspuns corect: -> `a`
### Subiectul II

1. 
    - a =>
        ```json
            n = 252
            d = 2, x = 1, y = 1
            cat timp 252 > 1 executa
                daca 252 % 2 == 0
                    x = d => x = 2, y = 2
                    cat timp 252 % 2 == 0
                        n = 252 / 2 = 126
                    cat timp 126 % 2 == 0
                        n = 126 / 2 = 63
                    cat timp 63 % 2 == 0 => fals
                d = 3
            cat timp 63 > 1
                daca 63 % 3 == 0
                    x = 3; y = 6
                    cat timp 63 % 3 == 0
                        n = 63/3 = 21
                    cat timp 21 % 3 == 0
                        n = 21 /3 = 7
                    cat timp 7 % 3 == 0 fals
                d = 4
            cat timp 7 > 1
                daca 7% 4 == 0 fals
                d = 5
            cat timp 7 > 1
                daca 7 % 5 == 0 fals
                d = 6
            cat timp 7 > 1
                daca 7% 6 == 0 fals
                d = 7
            cat timp 7 > 1
                daca 7 % 7 == 0
                    x = 7; y = 6 * 7 = 42
                    cat timp 7%7 == 0
                        n = 7 / 7 = 1
            cat timp 1 > 1 fals

            scrie 7 ' ' 42
        ```
    - b =>
        ```json
            Programul de mai sus afiseaza prin x ultimul factor prim descoperit si prin y produsul factorilor primi distincti aia lui n
            Numere din intervalul 10-100 care are un singur factor prim: 
                16
                32
        ```
    - c => 
        ```c++
            #include <iostream>
            using namespace std;

            int estePrim(int n);

            int main() {
                int n;
                cin >> n;
                int d = 2, x = 1, y = 1;
                while (n > 1) {
                    if (n%d == 0) {
                        x = d;
                        y = y * d;
                        while ( n % d == 0) {
                            n = n / d;
                        }
                    }
                    d++;
                }
                cout << x << " " << y;
                return 0;
            }

        ```
    - d =>
        ```json
            citeşte n
            (număr natural, n≥2)
            d<-2; x<-1; y<-1
            ┌cât timp n>1 execută
            │┌dacă n%d=0 atunci
            ││ x<-d; y<-y*d
            ││┌daca n%d = 0 atunci
            │││┌execută
            ││││ n<-[n/d]
            |||└■cât timp n%d=0 
            ||└■
            │└■
            │ d<-d+1
            └■
            scrie x,' ',y 
        ```
2. Rezolvare:
    ```c++
        f(17)
        x = 17
            if (x<=4) false
            else return 17 - f(15)
                x = 15
                    if(x<= 4) false
                    else return 15 - f(13)
                        x = 13
                            if (x <= 4) false
                            else return 13 - f(11)
                                x = 11
                                    if (x <= 4) false
                                    else return 11 - f (9)
                                        x = 9
                                            if (x <= 4) false
                                            else return 9 - f(7)
                                                x = 7
                                                    if (x <= 4) false
                                                    else return 7 - f(5)
                                                        x = 5
                                                            if (x <= 4) false
                                                            else return 5 - f(3)
                                                                x = 3
                                                                if (x <= 4) return 3
        17-15-13-11-9-7-5-4 doar ca facem de la capat adica
        17 - (15 - (13 - (11 - (9 - (7 - (5 - 3)))))) =
        17 - (15 - (13 - (11 - (9 - (7 - 2))))) =
        17 - (15 - (13 - (11 - (9 - 5)))) = 
        17 - (15 - (13 - (11 - 4))) = 
        17 - (15 - (13 - 7))
        17 - (15 - 6) = 
        17 - 9 = 8

        Pentru f(2) este simplu avem direct 2
        Raspuns corect: 2 si 8
    ```
3. Rezolvare:
    ```c++
        strcpy(s1,"parcarea"); // s1="parcarea"
        strcpy(s2,strstr(s1,"car")); //s2=carea
        n=strlen(s2); //n = 5
        strcpy(s1+n-2, s2+n-2); // asta devine strcpy(s1+3, s2+3)=> s1=parea
        //n = 5, s1=parea
    ```
### Subiectul III

1. Rezolvare:
    ```c++
        #include <iostream>

        using namespace std;

        void consecutiv(int n, int &f);

        int main() {
            int n = 19;
            int f;
            consecutiv(n, f);
            cout << f;
            return 0;
        }

        void consecutiv(int n, int &f) {
            int rezultat = 1;
            while (rezultat <=n) {
                if ((rezultat -1) * rezultat < n && n<= rezultat * (rezultat+1)) {
                    f = rezultat;
                    break;
                }
                rezultat++;
            }
        }
    ```
2. Rezolvare:
    - Aici avem doua variante.
        1. Varianta in care atunci cand parcurgem coloanele, mai facem un for care merge de la j-ul curent inca 3 pozitii in fata
            ```c++
                #include <iostream>

                using namespace std;

                int main() {
                    int nr,np;
                    cin>>nr>>np;
                    int parcare[nr][np];
                    for (int i =0; i<nr; i++) {
                        for (int j=0; j<np; j++) {
                            cin >> parcare[i][j];
                        }
                    }
                    int contorTriplete = 0;
                    for (int i = 0; i < nr; i++) {
                        if (i == 0 || i == nr-1) {
                            for (int j =0; j < np; j++) {
                                int existaTripleta = 1;
                                for (int k = j; k < j+3 && k < np ; k++) {
                                    if (parcare[i][k] == 1) {
                                        existaTripleta = 0;
                                        break;
                                    }
                                }
                                if (existaTripleta == 1) {
                                    contorTriplete++;
                                }
                            }
                        }
                    }
                    cout << contorTriplete << endl;
                    return 0;
                }
            ```
        2. Varianta in care nu mai facem un extra `for` si hardcodam valorile
            ```c++
                #include <iostream>
                using namespace std;

                int main() {
                    int nr, np;
                    cin >> nr >> np;
                    int parcare[51][51];  // dimensiuni maxime conform enunțului

                    for (int i = 0; i < nr; i++) {
                        for (int j = 0; j < np; j++) {
                            cin >> parcare[i][j];
                        }
                    }

                    int contorTriplete = 0;

                    // verificăm doar primul rând (i=0) și ultimul rând (i=nr-1)
                    for (int i = 0; i < nr; i++) {
                        if (i == 0 || i == nr-1) {
                            for (int j = 0; j <= np - 3; j++) { // mergem doar până la np-3
                                if (parcare[i][j] == 0 && parcare[i][j+1] == 0 && parcare[i][j+2] == 0) {
                                    contorTriplete++;
                                }
                            }
                        }
                    }

                    cout << contorTriplete << endl;
                    return 0;
                }
            ```
        - Alege varianta care ti se pare tie mai clara, sau propria ta varianta.
3. Rezolvare:
    - a
        ```json
            Observam ca enuntul problemei cere sa gasim 2 minime si cel mai mare numar din fisier.
            Inainte de a trece la rezolvarea propriu zisa a problemei, observam ca avem nevoie de a transforma fiecare numar din fisier in inversul sau. De aceea o sa scriu un subprogram care primeste un numar si intoarce inversul sau, pentru a ne usura logica ce urmeaza.
            Continuam cu declararea variabilele corespunzatoare pentru cele doua minime (minim1, minim2) si pentru valoarea maxima pe care o sa o gasim (maxim). minim1 si minim2 vor fi initializate cu valoarea 10.000 deoarece stim ca numerele din fisier au maximum valoarea 9999, pe aceleasi principiu, initializam variabila maxim cu 0 deoarece stim ca numerele noastre sunt mai mari sau egale cu 1001.
            Urmatorul pas este sa parcurgem fisierul, numar cu numar si aplicand logica urmatoare pentru fiecare numar:
                - Daca inversul numarului citit este mai mic decat minim1 atunci salvam in minim2 ce am avut in minim1 si in minim1 punem inversul.
                - Altfel daca inversul nmarului citit este mai mic decat minim2 atunci salvam in minim2, inversul numarului citit.
                - Daca inversul numarului citit nu este nici mai mic decat minim1, nici mai mic decat minim2, verificam daca este mai mare decat maxim, caz in care salvam in maxim valoarea inversului.

            Dupa ce am parcurs fisierul, mai facem o verificare, anume daca exista cel putin una dintre cele 3 variabile (minim1, minim2, si maxim) ale carei  valori nu a fost schimbata, atunci afisam "nu exista" altfel afisam numerele conform cerintei adica minim1, urmat de un spatiu, urmat de maxim, inca un spatiu si ultima oara, minim2.
            
            Algoritmul este eficient din punct de vedere al timpului de executie deoarece rezultatul este calculat dintr-o singura parcurgere a fisierului plus atunci cand intalnim valori pe care le avem
            deja salvate intr-una din cele 3 variabile, sarim peste iteratia respectiva. Totodata, algoritmul este eficient din punct de vedere al memoriei deoarece din totalul de 10^6 numere cate pot fi in fisier, noi tinem in memorie doar unul si nu folosim alte structuri de date pentru a stoca numerele.
        ```
    - b
        ```c++
                #include <iostream>
                #include <fstream>

                using namespace std;

                int construiesteInvers(int n);


                int main() {
                    ifstream fin("bac.in");
                    int minim1 = 10000,minim2=10000,maxim=0;
                    int numar;
                    while (fin >> numar) {
                        int invers = construiesteInvers(numar);
                        if (invers == minim1 || invers == minim2 || invers == maxim) continue;
                        if (invers < minim1) {
                            minim2 = minim1;
                            minim1 = invers;
                        } else if (invers < minim2) {
                            minim2 = invers;
                        } else if (invers > maxim) {
                            maxim = invers;
                        }
                    }

                    if (minim1 == 10000 || minim2 == 10000 || maxim == 0) {
                        cout << "nu exista";
                    } else {
                        cout << minim1 << " " << maxim << " " << minim2 << endl;
                    }
                    fin.close();
                    return 0;
                }

                int construiesteInvers(int n) {
                    int rezultat=0;
                    while (n > 0) {
                        int cifra = n % 10;
                        rezultat = rezultat * 10 + cifra;
                        n= n / 10;
                    }

                    return rezultat;
                }
        ```
## Rezolvare Varianta August 2025

- Link: https://www.pbinfo.ro/resurse/9dc152/examene/2025/E_D_Informatica_2025_sp_MI_C_var_04_LRO.pdf
### Subiectul I
1. 
    - Dupa aplicarea operatorului `!` expresia devine : `x > 2020 && x <= 2025` deci (2020,2025]
    - a => Adevarat
    - b => Fals! Intervalul e inchis la 2025
    - c => Fals! Intervalul e deschis la 2020
    - d => Fals! Intervalul e inchis la 2025
    - Raspuns corect: `A`
2. Rezolvare:
    ```c++
        strcpy(s,"calculator"); // s = "calculator"
        k=strchr(s,s[1])-strchr(s,s[3]); // acum sa spargem pe bucati aceasta expresie din interior catre exterior:
        s[3] = 'c'
        strchr(s,s[3]) = "calculator"
        s[1] = 'a'
        strchr(s,s[1]) = "alculator"
        k = 1 => Practic avem calculator - alculator si se scad pozitiile pointerilor.
    ```
    - Raspuns corect: `D`
3. Rezolvare:
    ```json
        Avem urmatoarele perechi:
        {A, B, C, D, E, F}
    
        Stiind ca perechea A este prima si perechea F este ultima practic avem:
    
        A _ _ _ _ F
    
        Primele 3 solutii sunt: 
        (A, B, C, D, E, F),
        (A, B, C, E, D, F),
        (A, B, D, C, E, F)
    
        Ultima solutie este:
    
        A E D C B F 
        Deoarece vedem ca solutiile generate sunt in ordine alfabetica deci intr-un final ajungem la solutia de mai sus.
    ```
    - Raspuns corect: `C`

4. Rezolvare:
    - Din graful de mai jos observam ca pentru urmatoarele noduri avem acelasi grad interior/exterior:
        ![Nod 6 radacina](imagini/august-s1-e4.png)
          - 3 - grad interior 1 / grad exterior 1
          - 6 - grad interior 1 / grad exterior 1
      - Raspuns corect: `B`
5. Rezolvare 
    - Deoarece avem 50 de noduri, excludem varianta de a desena acest graf. Este prea mult si ne-ar incurca.
    - Trebuie sa gasim rezolvarea in alt mod.
    - Lant elementar: Lanțul care conține numai vârfuri distincte, două câte două, este lanț elementar.
    - Si conform enuntului unde parintele unui nod i este nodul [i/2] deci pentru lantul elementar care incepe in 32 si se termina in 23 o aflam parcurgand urmatorii pasi:
    - Parinti pentru 32 => 16 - 8 - 4  - 2  - 1
    - Parinti pentru 23 => 11 - 5 - 2 - 1

    - Deci lantul elementare ar merge => 32 - 16 - 8 - 4 - 2 - 5 - 11 - 23
    - Cel mai de jos stramos comun este 2 apare in ambele liste.
    - Distanta (numarul de muchii intre doua noduri) => 7
    - Raspuns corect:  `B`

### Subiectul II
1. Rezolvare
    - a
        ```json
            x = 9767, y = 8204
            cx = 0, cy = 0;
            cat timp x >= 10 sau y >= 10 executa
                cat timp x+y != 0 executa
                    cx = 0 + 7 = 7; x = 976
                    cy = 0 + 4 = 4; y = 820
                cat timp x+y != 0 executa
                    cx = 7 + 6 = 13; x = 97
                    cy = 4 + 0 = 4; y = 82
                cat timp x+y != 0 executa
                    cx = 13 + 7 = 20; x = 9
                    cy = 4 + 2 = 6; y = 8
                cat timp x+y != 0 executa
                    cx = 20 + 9 = 29; x = 0
                    cy = 6 + 8 = 14; y = 0
                cat timp x+y != 0 fals
        
            cat timp x >= 10 sau y >= 10 executa
                cat timp x+y != 0 executa
                    cx = 0 + 0 = 0; x = 2;
                    cy = 0 + 4 = 4; y = 1
                cat timp x+y != 0 executa
                    cx = 0 + 2 = 2; x = 0;
                    cy = 4 + 1 = 5; y = 0
                cat timp x+y != 0 fals
        
            x = 2; cx = 0; y = 5; cy = 0;   
            
            daca x = y -> false -> scrie "NU 2 5"
        ```
        - Răspuns corect: NU 2 5 
    - b
       - Daca avem x = 2025 si dorim sa fie afisat "DA" trebuie pentru y sa alegem numere care au suma cifrelor egala cu suma cifrelor numarului 2025 adica 9 (sau 18 deoarece facem suma sumelor cifrelor). si trebuie sa alegem din intervalul [10,99]
           - 72 si 18
    - c
       ```c++
            #include <iostream>
            using namespace std;
            
            int main() {
            
            int x, y;
            cin >> x >> y;
            int cx = 0, cy = 0;
            while (x >= 10 || y >= 10) {
                while (x+y != 0) {
                    cx = cx + x % 10;
                    x = x / 10;
                    cy = cy + y % 10;
                    y = y / 10;
                }
            
                x = cx;
                cx = 0;
                y = cy;
                cy = 0;
            }
            
            if (x == y) {
                cout << "DA " << x;
            } else {
                cout << "NU " << x << " " << y;
            }
            return 0;
            }

       ```
    - d
        ```json
             citeşte x,y
             (numere naturale distincte)
             cx<-0; cy<-0
            
             ┌daca x≥10 sau y≥10  atunci
             │┌execută
             ││┌cât timp x+y≠0 execută
             │││ cx<-cx+x%10; x<-[x/10]
             │││ cy<-cy+y%10; y<-[y/10]
             ││└■
             ││ x<-cx; cx<-0; y<-cy; cy<-0
             │└■ cât timp x≥10 sau y≥10 
             └■
            ┌dacă x=y atunci scrie "DA ",x
            │altfel scrie "NU ",x," ",y
            └■
        ```
2. Rezolvare:
    ```json
        f(3,9) => il putem calcula direct deoarece 3*5 > 9/5 deci intram in primul if si afisam direct 3
        f(1,1000) =
            X = 1;Y=1000 => 1*5 > 1000/5 => FALS => calculam f(5, 200)
            f(5,200) =
                x = 5;y = 200 => 5 * 5 > 200/5 FALS => calculam f(25, 40)
                f(25,40) =
                    x = 25; y = 40 => 25 * 5 >40 /5 => returnam 25;
    ```
3. Rezolvare
    ```c++
        #include <iostream>
        #include <cstring>
        using namespace std;
    
        // Nota: doar ce este intre linii trebuie sa scrii pe foaia de la bac
        //-----------------------------------
        struct bijuterie {
            int greutate;
            struct {char denumire[31]; int pret; } metal;
        }b;
        //----------------------------------
        int main() {
    
            // Nota: partea de mai jos nu trebuie sa o scrii la bac. Eu o fac doar ca sa testez ca totul merge bine.
            strcpy(b.metal.denumire, "aur");
            b.metal.pret = 100;
            b.greutate = 121;
    
            cout << b.greutate * b.metal.pret<<endl;
    
            return 0;
        }
    ```

### Subiectul III

1. Rezolvare:
    - Practic problema ne cere sa afisam divizorii pari care sunt stricti mai mari decat numar / divizor.
    - Mesajul formulat va fi de genul cout << divizorParCareRespectaCerinta << " parcele de arie " << numar / divizorParCareRespectaCerinta
    ```c++
        #include <iostream>

        using namespace std;
        
        void teren(int x, int y);
        
        int main() {
        
            teren(6,8);
        
            return 0;
        }
        
        void teren(int x, int y) {
            int arie = x * y;
            int exista = 0;
        
            for (int i = 2; i <= arie; i++) {
                if (arie % i == 0) {
                    int arieLot = arie / i;
                    if (i % 2 == 0 &&  i< arieLot) {
                        exista = 1;
                        cout << i << " parcele de arie " << arieLot << endl;
                    }
                }
        
            }
        
            if (exista == 0) {
                cout << " nu exista";
            }
        }

    ```
2. Rezolvare:
    - Practic problema presupune urmatorii pasi:
       - Identificarea valorii minime
       - Salvarea valorii pe care vrem sa o folosim cand vrem sa inlocuim
          - Nota: trebuie sa faci asta inainte de a incepe inlocuirea deoarece este posibil ca si in ultima coloana sa inlocuim.
        - Iteram prin matrice si cand gasim un element egal cu valoarea minima, inlocuim toate elementele de pe coloana sa cu elementul dorit. 
    ```c++
        #include <iostream>

        using namespace std;
                
        int main() {
        
            int m, n;
            cin >> m >> n;
            int matrice[m][n];
        
            for (int i = 0; i < m; i++) {
                for (int j = 0; j < n; j++) {
                    cin >> matrice[i][j];
                }
            }
        
            int minim = 101;
            for (int i = 0; i < m; i++) {
                for (int j = 0; j < n; j++) {
                    if (matrice[i][j] < minim) {
                        minim = matrice[i][j];
                    }
                }
            }
        
            int elementPentruInlocuire = matrice[m-1][n-1];
            for (int i = 0; i < m; i++) {
                for (int j = 0; j < n; j++) {
                    if (matrice[i][j] == minim) {
                        for (int k = 0; k < m; k++) {
                            matrice[k][j] = elementPentruInlocuire;
                        }
                    }
                }
            }
        
            for (int i = 0; i < m; i++) {
                for (int j = 0; j < n; j++) {
                    cout << matrice[i][j] << " ";
                }
                cout << endl;
            }
        
        
            return 0;
        }

    ```

3. Rezolvare:
    - a
        ```json
            O sa implementez un algoritm care mai intai va citi cele doua variabile minZ si minP dupa care va citi numar cu numar din fisier. Cu ajutorul unor variabile pe care le voi seta egale cu -1, voi salva pozitia de inceput a unei perioade si pozitia de sfarsit. Dupa aceea aplicam logica urmatoare:
            - Atunci cand intalnesc un stoc zilnic care este mai mare sau egal cu minZ ma voi uita daca trebuie sa marchez inceputul unei perioade (ziInceputPerioada == -1) caz in care initializez variabila ziInceputPerioada cu valoarea pozitiei stocului (pentru care avem un contor declarat), iar daca nu suntem la inceput de perioada, actualizam variabila ce tine pozitia de sfarsit a perioadei.
            - De asemenea pentru fiecare stoc zilnic valid, actualizam si suma pentru stocurile zilnice.
            - De fiecare data cand intalnim un stoc ce nu respecta conditia (>= minZ) ne uitam daca am intalnit deja o perioada (ziInceputPerioada si ziSfarsitPerioada trebuie sa fie diferite de -1 dar noi verificam doar variabila pentru sfarsit deoarece ea se actualizeaza dupa variabila de inceput) si ne mai uitam daca avem cel putin 2 zile in perioada (adica diferente dintre cele 2 pozitii sa fie mai mare decat 1) dar si daca suma stocului pentru perioada indeplineste conditia >= minP, si daca expreesia este adevarata afisez conform cerintei.
            - Indiferent daca expresia este evaluata sau nu cu true, resetez variabilele ce tin pozitia de inceput si sfarsit a perioadei, respectiv suma stocului zilnic.

        La final avem de facut 2 chestii:
            - 1 mai verificam inca o data daca avem sau nu o perioada valida pentru a acoperi cazul in care fisierul se sfarsteste cu o perioada valida
            - 2 de fiecare data cand afisam, setam un steag pe adevarata ca sa stim daca am intalnit sau nu cel putin o perioada valida. Daca nu am intalnit nici o perioada valida, afisam mesajul "nu exista"
        ```
    - b
        ```c++
            #include <iostream>
            #include <fstream>
            
            using namespace std;
            
            int main(){
            
                ifstream fin("bac.in");
                int minZ, minP;
                fin >> minZ >> minP;
            
                int contorZi = 0;
                int ziInceputPerioada = -1;
                int ziSfarsitPerioada = -1;
                int sumaStocPerioada = 0;
                int stocZilnic;
                int existaPerioada = 0;
                while (fin >> stocZilnic) {
                    contorZi++;
                    if (stocZilnic>=minZ) {
                        if (ziInceputPerioada == -1) {
                            ziInceputPerioada = contorZi;
                        } else {
                            ziSfarsitPerioada = contorZi;
                        }
                        sumaStocPerioada += stocZilnic;
                    } else {
                        if (sumaStocPerioada >= minP && ziSfarsitPerioada != -1 && (ziSfarsitPerioada - ziInceputPerioada > 1)) {
                            existaPerioada  = 1;
                            cout << ziInceputPerioada << " " << ziSfarsitPerioada <<  " " << sumaStocPerioada << endl;
                        }
                        ziInceputPerioada = -1;
                        ziSfarsitPerioada = -1;
                        sumaStocPerioada = 0;
                    }
                }
            
                // Mai facem o verificare pentru a fi siguri ca prindem si cazul cand la final, ultimele numere
                // reprezinta o perioada valabila
                if (sumaStocPerioada >= minP && ziSfarsitPerioada != -1 && (ziSfarsitPerioada - ziInceputPerioada > 1)) {
                    existaPerioada  = 1;
                    cout << ziInceputPerioada << " " << ziSfarsitPerioada <<  " " << sumaStocPerioada << endl;
                }
            
                if (existaPerioada == 0) {
                    cout << "nu exista";
                }
                fin.close();
                return 0;
            }
        ```

- Tema pentru sesiunea urmatoare:

    * Rezolvare varianta sesiunea speciala bac 2025: https://www.pbinfo.ro/resurse/9dc152/examene/2025/E_d_Informatica_2025_sp_MI_C_var_06_LRO.pdf 



