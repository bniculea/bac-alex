# Sesiunea 19

## Agenda
- Rezolvare varianta simulare 2026 Bihor
- Rezolvare varianta simulare 2026 Suceava


## Rezolvare Simulare Bihor 2026

### Subiectul I

1. Rezolvare
    - -17 % 5 = -2
    - Raspuns corect: `A`
2. Rezolvare
    - Calculam pe rand rezultatele
    ```json
        a)
        f(5, 87654)
            return f(5, 17530) + 4
                return f(5, 3506) + 0
                    return f(5, 701) + 1
                        return f(5, 140) + 1
                            return f(5, 28) + 0
                                return f(5,5) + 3
                                    return f( 5,1)+0
                                        return 1
        = 10 -> Incorect

        b)
        f(10, 87654)
            return f(10, 8765) + 4
                return f(10, 876) + 5
                    return f(10, 87) + 6
                        return f(10, 8) + 7
                            return 8
        = 30 => raspuns corect
    ```
    - Raspuns corect: `B`
3. Rezolvare
    - Observam ca singura varianta corecta d.p.d.v sintactic este `A[0]= B;`
    - Rapuns corect: `A`
4. Rezolvare
    - Din enunt avem urmatorul graf de mai jos:
        ![Graf final](imagini/s1-e4.png)
    - Observam ca avem 2 noduri care sunt legate cu un singur alt nod deci daca ar fi sa stergem de exemplu fie 5, fie 2, nodurile 1 si/sau 6 ar ramane izolate.
    - Daca adaugam fix muchia 6-1, atunci indiferent ce nod am sterge, subgraful si-ar pastra proprietatea de conexitate.

5. Rezolvare
    - Din vectorul de tati obtinem arborele de mai jos astfel:
    ```json
        1  2  3  4  5  6  7  8  9  10  11 12
        7, 6, 5, 2, 0, 5, 5, 6, 8, 2,  6, 8

        Radacina: 5
        5 parinte pentru: 3,6,7
        6 parinte pentru: 2,8,11
        7 parinte pentru: 1
        2 parinte pentru: 4, 10
        8 parinte pentru: 9, 12
    ```
     ![Graf final](imagini/s1-e5.png)
    - Din arbore obserbam ca nodurile care respecta cerinta sunt 2 si 8
    - Raspuns corect: `D`
### Subiectul II
1. 
    a. Rezolvare:
        ```c++
            n = 175450
            ans = 0
            p = 2
            daca n % 2 = 0
                ans = 1
                n = n/2 = 87725
            cat timp p <= n executa
                daca p * p > n fals
                e = 0
                cat timp n % p == 0 fals
                ans = ans * (e+1) = 1
                p = 3
            cat timp p <= n executa
                daca p * p > n fals
                e = 0
                cat timp n % p == 0 fals
                ans = ans * (e+1) = 1 * 1 = 1;
                p = 4;
            cat timp p <= n executa
                daca p * p > n fals
                e = 0
                cat timp n%p == 0 fals
                ans = 1
                p = 5
            cat timp  p <= n executa
                daca p * p > n fals
                e = 0
                cat timp n%p = 0 executa
                    e = 1
                    n = n/p = 17545
                cat timp n%p == 0 executa
                    e = 2
                    n = n/p = 3509
                cat timp n%p == 0 fals
                ans = 1 * 3 = 3
                p = 6
            cat timp p <= n
                daca p * p > n fals
                e =0
                cat timp n%p == 0 fals
                ans = 3
                p = 7
            cat timp p<= n
                daca p * p > n
                e = 0
                cat timp n%p == 0 fals
                ans = 3
                p = 8
            
            cat timp p<= n
                daca p*p > n
                e =0 
                cat timp n%p == 0 fals
                ans = 3
                p = 9
            cat timp p<= n
                daca p*p > n
                e = 0
                cat timp n%p == 0 fals
                ans = 3
                p = 10
            cat timp p<= n
                daca p*p > n
                e = 0
                cat timp n%p == 0 fals
                ans = 3
                p = 11
            cat timp p<= n
                daca p * p > n
                e = 0
                cat timp n%p == 0
                    e = 1
                    n = n/p = 319
                cat timp n% p == 0
                    e = 2
                    n = n/p = 29
                ans = 3 * 3 = 9
                p = 12
            cat timp p <= n
                daca p * p > n 
                    p = 29
                e =  0
                cat timp n%p == 0
                    e = 1
                    n = 1
                ans = 9 * 2 = 18
            cat timp p <= n fals
            scrie: 18
        ```
    b. Rezolvare:
        - Algoritmul calculeaza un produs calculat pe baza numarului de divizari succesive ale lui n la fiecare divizor
        - Pentru a obtine 2 inseamna ca avem un numar care trebuie sa se imparta la 2 dupa care sa fie prim:
            - 106 (106/2 => 53 -> prim)
            - 998 (998/2 => 499 -> prim)
    c.
        ```c++
            #include <iostream>
            using namespace std;

            int main() {

                int n;
                cin >> n;
                int ans = 0, p = 2;
                if (n% 2 == 0) {
                    ans = 1;
                    n = n / 2;
                }

                while (p<= n) {
                    if (p * p > n) {
                        p = n;
                    }
                    int e = 0;
                    while (n%p == 0) {
                        e = e+1;
                        n = n / p;
                    }
                    ans = ans * (e+1);
                    p = p + 1;
                }
                cout << ans;

                return 0;
            }
        ```
    d.  Rezolvare
        ```c++
            citește N
            ans<-0, p<-2;
            ┌dacă N%2=0 atunci
            │ans<-1, N<-[N/2]
            └■
            ┌pentru p<2,N execută
            │┌dacă p*p > N atunci p<-N
            │└■
            │e<-0
            │┌cât timp N%p=0 execută
            ││e<-e+1, N<-[N/p]
            │└■
            │ans<-ans*(e+1)
            │
            └■
            scrie ans
        ```
2. Rezolvare
    ```json
        primele patru soluții generate sunt: 
        (14,3,2,1)
        (13,4,2,1)
        (12,5,2,1)
        (12,4,3,1)

        (10,5, 3, 2) <- inainte
        (9, 8, 2, 1)
        (9, 7, 3,1) <- dupa
    ```
    - Observam in exemplul lor ca se incearca sa se dea mai mult locului 1 dupa care dam valorile cat mai mici posibile pentru celelalte locuri

3. Rezolvare
    ```c++
        #include <iostream>
        using namespace std;

        int main() {
            int a[6][6];
            int i, j;

            // La bac scrie doar ce e intre liniile punctate
            // Observam ca pe diagonala secundara avem 3
            // Iar in stanga diagonalei secundare scadem dar in dreapta crestem insa uneori se dubleaza valoarea, alteori nu, in ambele parti
            // deci incercam sa cautam o alta varianta
            /*
            *  Fiecare 2 linii consecutive sunt identice
            Fiecare 2 coloane consecutive sunt identice
            Valoarea crește cu 1:

                când treci la următorul „bloc” de 2 linii

                sau la următorul „bloc” de 2 coloane
                deci inseamna ca putem sa ne folosim de faptul ca atunci cand avem numere care impartite la o valoare, dau cu virgula si sunt trunchiate
                de exemplu pe linia 2 (de la 0 incepem numerotarea) si coloana 2 avem 3 si 3 l-am putea obtine adunand:
                    (i+2 +j+2) / 2 - 1 => 4 - 1 = 3
                    si la urmatorul trei am avea
                    (i+2 + j+2) / 2 - 1 => (4 + 5) / 2 -1 = 9/2 -1 = 3
                    de asemenea putem simplifica formula in: a[i][j] = (i+2 + j+2)/2 - 1;
            */
            //------------------------------
            for(i=0;i<6;i++)
                for(j=0;j<6;j++)
                a[i][j] = (i+2 + j+2)/2 - 1;

            //------------------------------
            for(i=0;i<6;i++) {
                for(j=0;j<6;j++) {
                    cout<<a[i][j]<<" ";
                }
                cout<<endl;
            }


            return 0;
        }

    ```
### Subiectul III

1. Rezolvare:
    ```c++
        #include <iostream>
        using namespace std;

        int prodFact(int N, int M);

        int main() {

            cout << prodFact(5, 7) << endl;
            cout << prodFact(2, 5) << endl;
            return 0;
        }

        int prodFact(int N, int M) {
            int minProd = 0;

            // cautam toate produsele i * j cu 1 <= i,j <= N
            for (int i = 1; i <= N; i++) {
                for (int j = 1;j<=N; j++) {
                    int produs = i * j;
                    if (produs >= M) {
                        if (minProd == 0 || produs < minProd) {
                            minProd = produs;
                        }
                    }
                }
            }
            return minProd;
        }
    ```
    // Acum si o varianta imbunatatita unde pentru fiecare i, calculam direct cel mai mic j valid si nu mai facem o bucla interioare adica din O(n^2) obtinem O(n)
    ```c++
        #include <iostream>
        using namespace std;

        int prodFact(int N, int M);

        int main() {

            cout << prodFact(5, 7) << endl;
            cout << prodFact(2, 5) << endl;
            return 0;
        }

        int prodFact(int N, int M) {
            int minProd = 0;

            for (int a = 1; a <= N; ++a) {
                // calculăm b minim pentru care a*b >= M
                int b = (M + a - 1) / a; // echivalent cu ceil(M/a)
                if (b > N) continue;      // nu există b valid
                int p = a * b;
                if (minProd == 0 || p < minProd) minProd = p;
            }

            return minProd;
        }
    ```
2.  Rezolvare
    ```c++
        #include <cstring>
        #include <iostream>
        using namespace std;

        int numaraCifre(int n);
        int main() {
            char text[100];
            cin.getline(text, 100);
            char rezultat[100]="";
            char* cuvant = strtok(text, " ");
            while (cuvant != NULL) {
                if (strlen(cuvant) > 9) {
                    int pozitie = 0;
                    char comprimat[5]="";
                    comprimat[pozitie++] = cuvant[0];
                    int lungimeCuvant = strlen(cuvant);
                    int numarCifreLungime = numaraCifre(lungimeCuvant);
                    while (lungimeCuvant > 0) {
                        int ultimaCifra = lungimeCuvant % 10;
                        comprimat[numarCifreLungime] =  (ultimaCifra + '0');
                        numarCifreLungime--;
                        lungimeCuvant /= 10;
                        pozitie++;
                    }
                    comprimat[pozitie]=cuvant[strlen(cuvant)-1];
                    strcat(rezultat, comprimat);
                }else {
                    strcat(rezultat, cuvant);
                }
                strcat(rezultat, " ");
                cuvant = strtok(NULL, " ");
            }

            cout << rezultat << endl;
            return 0;
        }

        int numaraCifre(int n) {
            int contor = 0;
            while (n > 0) {
                contor++;
                n = n/10;
            }
            return contor;
        }
    ```
3. Rezolvare
    - a
        ```json
            O sa implmentam un algoritm care va mai intai va citi din fisier cele doua numere, n si x, apoi celelalte n numere. In timp ce o sa citim numerele, pentru fiecare numar citit, o sa tinem in memorie si numarul anterior, unde vom verifica daca suma numarului curent cu cel anterior este mai mare decat x atunci o sa calculam numarul de bomboane ce trebuiesc scoase, folosind formula (numarCurent + numarAnterior) - x;, valoare pe care nu doar ca o sa o scadem din numarul curent, dar o sa tinem minte intr-un contor, numarul total de bomboane scoase. Dupa care, la finalul fiecarei iteratii in cadrul careia vom citii un numar nou, o sa actualizam si valoarea din variabila ce tine numarul anterior.
            La final, algoritmul va afisa valoarea salvata in contorul in care am tinut numarul total de bomboane scoase.
            Algoritmul este eficient din puncte de vedere al timpului de executie deoarece acesta are o complexitate liniara (O(n)) si totodata, este eficient din punct de vedere al memoriei deoarece din totalul de 10^5 numere cate pot fi in fisier pe a doua linie, noi in memorie o sa tinem doar 2, in orice moment, nefolosind alte structuri de
        ```
    - b
        ```c++
            #include <iostream>
            #include <fstream>

            using namespace std;

            int main() {
            ifstream fin("bac.txt");
            int n, x;
            fin >> n >> x;
            int bomboaneScoaseInTotal =0;
            int numarCurent;
            int numarAnterior;
            fin >> numarCurent;
            numarAnterior = numarCurent;
            while (fin >> numarCurent) {
                if (numarCurent + numarAnterior > x) {
                    int bomboaneScoase = (numarCurent + numarAnterior) - x;
                    numarCurent -= bomboaneScoase;
                    bomboaneScoaseInTotal += bomboaneScoase;
                }
                numarAnterior = numarCurent;
            }

            cout << bomboaneScoaseInTotal << endl;
            return 0;
            }
        ```

## Rezolvare subiecte simulare Suceava 2026

### Subiectul I
1. Rezolvare
    ```json
        - Observam intreaga expresie si ne uitam ca la final se face o inmultire cu 2 si se ia ultima cifra.
        - Acum daca ar sa inmultim orice numar cu 2, obtinem o cifra para si cifra maxima pe care o putem obtine este 8.
    ```
    - Raspuns corect: `B`
2. Rezolvare
    ```c++
        f(146563)
            if n == 0 FAls
            if (n%2) return 1 + f(14656)
                f(14656)
                    if(n == 0) fals
                    if (n % 2) fals
                    return f(1465)
                        if (n == 0) fals
                        if (n % 2)
                            return 1 + f(146)
                                f(146)
                                    if (n == 0) fals
                                    if (n % 2) fals
                                    return f(14)
                                        if (n == 0) fALS
                                        if (n % 2) fals
                                            return f(1)
                                                if (n == 0) fals
                                                if (n % 2)
                                                    return 1 + f(0) = 1
        = 3
    ```
    - Raspuns corect: `C`
3. Rezolvare
    ```json
        Primele 4 numere sunt:
        
        101,
        103,
        105
        121

        Ca sa o luam pe scurtatura ne uitam care e ultimul numar generat:
        545
        Deci penultimul este 543
        Daca ne uitam, am redus la o singura varianta adica a
    ```
    - Raspuns corect:  `A`
4. Rezolvare
    ```json
        - Intr-un graf complet avem legatura de la fiecare nod la toate celalte deci pentru fiecare nod avem n-1 muchii.
        - Noi stim ca avem un graf cu 5 noduri deci pentru fiecare nod avem gradul 4
    ```
    - Raspuns corect `D`
5. Rezolvare
    ```json
        Practic ne uitam dupa frunze si vedem care sunt frunzele cu care putem construi cele mai lungi drumuri.
        Avem 5 frunze dintre care 4 le putem folosi sa construim lanturile
        Deci raspuns corect 4. (pentru fiecare dintre cele 2 frunze din stanga avem 2 drumuri. 2x2=4)
    ```

### Subiectul II
1. 
    - a 
        - Rezolvare
        ```json
            Observam ca algoritmul numara cate dintre numerele introduse au cel putin o cifra mai mare decat primul numar introdus
        ```
        - Programul afiseaza 4
    - b 
        - Rezolvare
            - Tinand cont de explicatia de mai sus, un set de numere potrivite ar fi:
                - 3 12 1 121 1 212 0
                - Adica numere care sa nu aiba cifre mai mari ca 3.
    - c
        - Rezolvare
            ```c++
                #include <iostream>

                using namespace std;

                int main() {
                    int a;
                    cin >> a;
                    int q = 0;
                    int x;
                    do {
                        cin >> x;
                        int y = x;
                        while (y != 0) {
                            if (y % 10 > a) {
                                q = q+1;
                                y = 0;
                            } else {
                                y = y / 10;
                            }
                        }
                    } while (x != 0);
                    cout << q;
                    return 0;
                }
            ```
    - d 
        - Rezolvare
            ```json
                citește a (nr. natural, a<10) 
                q <- 0 
                citeşte x (nr. natural) 
                ┌ execută 
                │   y <- x 
                │   ┌ cât timp y ≠ 0 execută 
                │   │   ┌ dacă y%10 > a atunci 
                │   │   │   q <- q+1 
                │   │   │ y <- 0 
                │   │   │ altfel 
                │   │   │   y <- [y/10]  
                │   │   └■ 
                │   └■ 
                |   citeşte x (nr. natural) 
                └ cât timp x<>0 
                scrie q
            ```

2. Rezolvare
    ```c++
        struct Nota {
            char disciplina[31];
            int valoare
            struct {
                int zi;
                int luna;
                int an;
            } data;
        }N[30];
    ```
3. Rezolvare
    ```c++
        char s[30] = "simulareBACINFO", aux[30] = "";  //s = simulareBACINFO
        strcpy(aux, strchr(s, 'B')); // aux = BACINFO
        s[8] = NULL; // s=simulare
        strcpy(aux + 3, "-");  // aux=BAC-
        strcat(aux, s);  // aux = BAC-simulare
        cout << aux; // afiseaza BAC-simulare
    ```

### Subiectul III
1. Rezolvare
    ```c++
        #include <iostream>

        using namespace std;
        int strict_semiprim(int n);

        int main() {
            cout << strict_semiprim(6) << endl;
            cout << strict_semiprim(15) << endl;
            cout << strict_semiprim(10) << endl;
            cout << strict_semiprim(8) << endl;
            cout << strict_semiprim(12) << endl;
            cout << strict_semiprim(30) << endl;
            return 0;
        }

        int strict_semiprim(int n) {
            int contorDivizori = 0;
            for (int i = 2;i*i <= n;i++) {
                if (n % i == 0) {
                    contorDivizori++;
                    int putere = 0;
                    while (n % i == 0) {
                        putere++;
                        n = n / i;
                    }
                    if (putere != 1) {
                        return 0; // avem nevoie doaR de factori primi la puterea 1
                    }
                }
            }
            if (n > 1) {
                contorDivizori++;
            }
            return contorDivizori == 2;
        }
    ```
2. Rezolvare
    ```c++
        #include <iostream>

        using namespace std;
        int strict_semiprim(int n);

        int main() {
            int matrice[100][100];
            int n;
            cin >> n;
            for (int i = 0; i < n; i++) {
                for (int j = 0; j < n; j++) {
                    cin >> matrice[i][j];
                }
            }

            for (int i = 0; i < n; i++) {
                for (int j = 0; j < n; j++) {
                    // Doar daca suntem in zona de vest, atunci facem mutarile
                    if (i < j && i+j > n - 1) {
                        int aux = matrice[i][j];
                        // Observam ca atunci cand schimbam, elementele sunt pe aceeasi linie deci pastram i-ul
                        // si pentru coloana observam formula de mai jos, dupa ce am urmarit pe foaie cum evolueaza indicii
                        matrice[i][j] = matrice[i][n-1-j];
                        matrice[i][n-1-j] = aux;
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

        int strict_semiprim(int n) {
            int contorDivizori = 0;
            for (int i = 2;i*i <= n;i++) {
                if (n % i == 0) {
                    contorDivizori++;
                    int putere = 0;
                    while (n % i == 0) {
                        putere++;
                        n = n / i;
                    }
                    if (putere != 1) {
                        return 0; // avem nevoie doaR de factori primi la puterea 1
                    }
                }
            }
            if (n > 1) {
                contorDivizori++;
            }
            return contorDivizori == 2;
        }
    ```
3. Rezolvare
    - a
        ```json
            Alex, trimite-mi un mesaj pe whatsapp cand ajungi aici. Cu textul "AM Citit" :)
        ```
    - b 
        ```c++
            #include <iostream>
            #include <fstream>
            using namespace std;

            int main() {
                ifstream fin("bac.in");
                int frecventa[82] = {0};
                int numar;
                while (fin >> numar) {
                    int produs = numar % 10;
                    while (numar > 9) {
                        numar = numar / 10;
                    }
                    produs *= numar;
                    frecventa[produs]++;
                }
                int contor = 0;
                for (int i = 0; i < 82;i++) {
                    if (frecventa[i] > 0) {
                        contor++;
                    }
                }
                cout << contor << endl;
                return 0;
            }
        ```