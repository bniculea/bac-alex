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