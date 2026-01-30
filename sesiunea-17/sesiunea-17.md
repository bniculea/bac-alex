# Sesiunea 17

## Agenda
    
- Rezolvare Simulare Cluj
- Altele

## Rezolvare Simulare Cluj

### Subiectul I

1. Rezolvare
    - a - Corect dpdv sintactic
    - b - Corect din punct de vedere sintactic (rezultatul unei operatii logice este 1 sau 0)
    - c - INCORECT => Nu se poate aplica operatorul modulo (%) pe numere cu virgula
    - d - Corect dpdv sintactic
2. Rezolvare
    ```C
        
        f(5)
        ***x = 5
        while x > 1
            x = x-1 = 4
            f(3)
                ***x = 3
                while (x > 1)
                    x = 2
                    f(1)
                        x = 1
                        while 1> 1 - fals
                        cout << 1
                ***x=2
                while ( x > 1)
                    x = 1
                    f(0)
                        while(0 > 1) - fals
                        cout << 0
                ***x=1
                while 1>1 - fals
                        cout << 1
        ***x=4
        while x > 1
            x= 3
            f(2)
                ***x=2
                while(x > 1)
                    x = 1
                    f(0)
                        cout << 0 
                ***x=1
                while(1 > 1)
                cout << 1 
        ***x=3
        while (x > 1)
            x = 2
            f(1)
                cout << 1;
        
        ***x=2
        while (x > 1) 
            x = 1
            f (0)
              cout << 0 
        ***x=1
        while (1 > 1)
            cout << 1

    ```
    - Raspuns corect: `C`
3. Rezolvare:
    ```json
        - Prima: 2+2+2+3
        - A doua: 2+2+5
        - A treia: 2 + 7
    ```
    - Raspuns corect: `A`
4. Rezolvare
    - Se deseneaza arborele si se obtine ca nodul 7 are 5 descendenti
    - Raspuns corect: D
5. Rezolvare
    - Din enunt avem urmatorul graf initial
    * ![Poza graf](imagini/cluj-s1-e5-initial.png)
    - Daca din fiecare graf am duce din fiecare nod catre toate celelalte noduri din grafurile din dreapta am avea asa:
        - Nodul 1 merge in 6 alte noduri din dreapta
        - Nodul 2 merge in 6 alte noduri din dreapta
        - Nodul 3 merge in 6 alte noduri din dreapta
        - Nodul 5 merge in 3 alte noduri din dreapta
        - Nodul 4 merge in 3 alte noduri din dreapta
        - Nodul 6 merge in 3 alte noduri din dreapta
        - Nodurile 7,8,9 nu pot sa se duca catre celealte componente conexe deoarece ar invalida conditia de a avea 3 componente tare conexe
        - Deci pana acum avem 3 * 6 + 3 * 3 = 27 de extra arce. 
        - Observam ca in fiecare compoonenta conexa din imagine putem dubla fiecare arc si astfel mai obtinem inca 9 arce
        - In total: 27+9 = 36
        - Raspuns corect: `B`
### Subiectul II
1. Rezolvare
    - a
        ```json
            a = 12, b = 48
            p = 1
            d = 2
            cat timp d <= a si d<= b executa
                n = 0
                cat timp a%d = 0 si b%d = 0 executa
                    p = p * d = 1 * 2 = 2
                    n = n+1 = 0+1 = 1
                    a = a/d = 12/2 = 6
                    b = b/2 = 48 / 2 = 24
                cat timp a%d = 0 so b % d = 0 executa
                    p = p * d = 2 * 2 = 4
                    n = n+1 = 1 + 1 = 2
                    a = a / d = 6/2 = 3
                    b = b/d = 24/2 = 12
                cat timp a%d = 0 si b % d = 0 executa -> fals

                daca n%2 = 1 fals
                d = d+1 = 3
            cat timp d <= a si d<= b executa
                n = 0;
                cat timp a%d = 0 si b%d = 0
                    p = p * d = 4 * 3 = 12
                    n = n +1 =1
                    a = a / d = 3 / 3  = 1;
                    b = b / d = 12 / 3 = 4
                cat timp a%d = 0 si b%d = 0 fals
                daca n % 2 = 1
                    p =p / d = 12 / 3 = 4
                d = d+1 = 4
            cat timp d <= a si d<= b fals
            scrie p = scrie 4
        ```
        - Raspuns 4.
    - b Rezolvare
        ```json
            - Programul calculeaza produsul tuturor factorilor primi luati la putere maxima, adica CMMMC
            - Putem lua: 
                - 18, 36
                - 27 si 45
            - Practic orice pereche unde 9 le divide pe ambele
        ```
    - c Rezolvare
        ```c++
            #include <iostream>

            using namespace std;
            int main(){

                int a, b;
                cin >> a >> b;
                int p = 1;
                int d = 2;
                while (d <= a && d <=b) {
                    int n = 0;
                    while (a % d == 0 && b % d == 0) {
                        p = p * d;
                        n = n + 1;
                        a = a/d;
                    }
                    if ( n % 2 == 1) {
                        p = p / d;
                    }
                    d = d+1;
                }
                cout << p;
                return 0;
            }

        ```
    - d
        ```json
            citește a,b (numere naturale nenule)
            p←1
            d←2
            cât_timp d≤a și d≤b execută
                n←0
                daca a%d=0 și b%d=0 atunci 
                    repeta
                        p←p*d
                        n←n+1
                        a←[a/d]
                        b←[b/d]
                    pana cand a%d != 0 sau b%d != 0 
                dacă n%2=1 atunci
                    p←[p/d]
                Sfârșit_dacă
                d←d+1
            sfarsit_cât_timp
            scrie p
        ```
2. Rezolvare
    - graf neorientat conex => inseamna ca nu are noduri izolate
    - graf eulerian => Se numește graf eulerian un graf care conține un ciclu eulerian. Se numește ciclu eulerian un ciclu care conține toate muchiile grafului.
    - graf hamiltonian => graf hamiltonian un graf care conține un ciclu hamiltonian. Se numește ciclu hamiltonian un ciclu elementar care conține toate vârfurile grafului.
    - ciclu elementar =>  Se numește ciclu un lanț simplu în care primul vârf este identic cu ultimul. Dacă toate vârfurile sunt distincte, mai puțin primul și ultimul, se numește ciclu elementar.
    - Exemplu de lista:
        ```json
            1: 2 3
            2: 1 3
            3: 1 2 4 6
            4: 3 5
            5: 4 6
            6: 3 5 7
            7: 6
        ```
    * NOTA: Regula de aur:
        Un graf neorientat este eulerian ⇔ este conex și toate nodurile au grad PAR
3. Rezolvare
    ```c++
        #include <iostream>

        using namespace std;
        int main(){
            int i, j;
            int a[7][6];

            // La BAC trebuie sa scrii doar ce este intre liniile punctate
            //-----------------------------------------
            for(i=0;i<7;i++)
                for(j=0;j<6;j++) {
                    if (i % 2 == 0) {
                        a[i][j] = i * 6 + j + 1;
                    } else {
                        a[i][j] = (i+1) * 6 -j;
                    }
                }
            //------------------------------------------
            for (int i = 0; i < 7; i++) {
                for (int j = 0; j < 6; j++) {
                    cout << a[i][j] << " ";
                }
                cout << endl;
            }
            return 0;
        }

    ```
### Subiectul III
1. Rezolvare
    ```c++
        #include <iostream>

        int sub(int v[], int n);

        using namespace std;

        int main(){
            int n = 12;
            int v[12] = {21, 412, 2, 2026, 208, 523, 7, 128, 3174, 2026, 46, 8};
            cout << sub(v, n);
            return 0;
        }

        int sub(int v[], int n) {
            int maximCalduros =-1;
            int pozitieMaximCalduros = -1;
            for (int i = 0; i < n; i++) {
                int numar = v[i];
                int ultimaCifra = numar % 10;
                int primaCifra = ultimaCifra;
                numar = numar / 10;
                while (numar > 0) {
                    primaCifra = numar % 10;
                    numar = numar / 10;
                }
                if (primaCifra % 2 == ultimaCifra % 2 && v[i] > maximCalduros) {
                    maximCalduros = v[i];
                    pozitieMaximCalduros = i+1;
                }
            }
            return pozitieMaximCalduros;
        }

    ```
2. Rezolvare
    ```c++
        #include <iostream>
        #include <cstring>

        using namespace std;


        int main(){
            char text[501];
            cin.getline(text, 501);
            char cuvinte[251][501];

            char rezultat[501]="";
            int lungimeMaxima = 0;
            char* cuvant = strtok(text, " ");
            int n = 0;
            while (cuvant != NULL) {
                int lungimeCuvant = strlen(cuvant);
                if (lungimeCuvant > lungimeMaxima) {
                    lungimeMaxima = lungimeCuvant;
                }
                strcpy(cuvinte[n++], cuvant);
                cuvant = strtok(NULL, " ");
            }

            for (int lu = 1; lu<= lungimeMaxima; lu++) {
                int pozitiiCuLungimeaLu[101], k = 0;

                for (int i = 0; i < n; i++) {
                    if (strlen(cuvinte[i]) == lu) {
                        pozitiiCuLungimeaLu[k++] = i;
                    }
                }
                // interschimbări
                for (int i = 0; i < k / 2; i++) {
                    char aux[21]; // din nou presupunere pt lungimea unui cuvant
                    strcpy(aux, cuvinte[pozitiiCuLungimeaLu[i]]);
                    strcpy(cuvinte[pozitiiCuLungimeaLu[i]], cuvinte[pozitiiCuLungimeaLu[k - 1 - i]]);
                    strcpy(cuvinte[pozitiiCuLungimeaLu[k - 1 - i]], aux);
                }
            }

            for (int i = 0; i < n; i++) {
                cout << cuvinte[i];
                if (i < n - 1) cout << " ";
            }

            return 0;
        }

    ```
3. Rezolvare
    - a
        ```json
            O sa implementam un algoritm care se bazeaza pe urmatoarea logic: doua numere a si b au suma divizibila cu p daca suma resturilor lor la impartirea cu p este 0 sau p
            (a + b) % k == 0, atunci (a % k + b % k) % k == 0.
            Astfel observam:
                1. Daca un numar are restul 0, atunci are nevoie de un alt numar cu restul 0
                2. Daca un numar are restul r, are nevoie de un numar cu restul complementar cu r adica p-r
            Mai intai, declaram un vector de frecventa unde vom numar frecventa fiecarui numar % p.
            Dupa care calculam contorul pentru primul caz, adica perechi formate din numere care se divid cu p (restul 0). Aici, din n numere, putem forma (n * n-1)/2 perechi
            Dupa care calculam numarul de perechi pentru cazul 2 unde cautam numerele cu restul complementar (adica perechile cu restul r si p-r). 
            Aici, pentru a evita duplicatele, o sa mergem doar pana la p/2
            Si in acest caz avem doua situatii:
                1. Cand restul este mai mic decat complement, adunam la contorul perechilor, freecventa resturilor egale cu r * frecventa resturilor egale cu complementul acestuia
                2. Cand r este egal cu complementul sau
                    - Aici ne referim la situatia unde r = p-r adica 2r=p adica r = p/2
                    - Deoarece r trebuie sa fie un numar intre (resturile sunt intregi) aceasta egalitate este posibila doar daca p este numar par. Daca p este impar, nu vom avea niciodata un rest egal cu complementul sau.
                    - Si formula pentru a numar este asemenea cu cea in care restul este 0.
            La final o sa afisam valoarea contorului care fiind initializat cu 0, va trata si cazul in care nu exista perechi.
            Algoritmul este eficient din punct de vedere al timpului de executie deoarece are o complexitate liniara.
        ```
    - b
        ```c++
            #include <iostream>
            #include <fstream>

            using namespace std;

            /**
            *  Doua numere a si b au suma divizibila cu p daca suma resturlor lor la impartirea cu p este 0 sau p;
            *  1. Daca un numar are restul 0, are nevoie de un alt numar cu restul 0
            *  2. Daa un numar are restul r, atunci are nevoie de un numar cu rest p-r
            */

            int main(){
                ifstream fin("bac.txt");
                int n, p;
                fin >> n >> p;
                int frecventaResturi[1001]={0};
                int numar;
                while (fin >> numar) {
                    frecventaResturi[numar % p]++;
                }

                long long contorPerechi = 0;

                //1. Perechi formate din numere care se divid la p (rest 0
                // Din k numere, putem forma k * (k-1)/2 perechi
                contorPerechi+= (frecventaResturi[0] * (frecventaResturi[0]-1))/2;

                //2 Perechi formate din resturi complementare (r si p-r)
                // Mergem pana la p/2 pentru a nu numar perechile de doua ori
                for (int i = 1; i<= p/2; i++) {
                    int complement = p - i;
                    if (i < complement) {
                        // Caz general: restul i se combina cu restul p - i;
                        contorPerechi += frecventaResturi[i] * frecventaResturi[complement];
                    } else if (i == complement) {
                        // Caz special: daca p este par si i = p/2 (ex.: p = 4, i = 2
                        // se combina intre ele ca la restul 0
                        contorPerechi += (frecventaResturi[i] * (frecventaResturi[i]-1))/2;
                    }
                }

                cout << contorPerechi << endl;
                return 0;
            }

        ```