# Sesiunea 23

- Agenda
    - Rezolvare varianta BAC August 2021
    - Recapitulare pentru BAC

## Rezolvare varianta BAC August 2021

### Subiectul I

1. Rezolvare
    - Aici trebuie sa tinem cont de procesul de aducere la acelasi numitor comun dar si de precedenta operatorilor.
    - Intotdeauna, pentru a fi siguri de ce operator este luat in calcul mai intai, putem folosi paranteze pentru a delimita clar.
    - Lucru ce se intampla si in varianta `d` care este cea corecta.
    - Celelalte variante, deoarece nu folosesc paranteze, precedenta (ordinea) operatiilor este data strict de operatorii folositi si astfel nu mai obtinem raspunsul cerut in enunt.
    - Easpuns corect: `D`
2. Rezolvare
    - Subprogramul calculează suma produselor dintre paritatea cifrei (n%2, care este 1 dacă cifra este impară și 0 dacă este pară) și valoarea cifrei (n%10)
    ```c++
        f(1234): Cifra este 4. 4 % 2 = 0. Rezultat: 0 * 4 + f(123) = 0 + f(123).
            f(123): Cifra este 3. 3 % 2 = 1. Rezultat: 1 * 3 + f(12) = 3 + f(12).  
                f(12): Cifra este 2. 2 % 2 = 0. Rezultat: 0 * 2 + f(1) = 0 + f(1).  
                    f(1): Cifra este 1. 1 % 2 = 1. Rezultat: 1 * 1 + f(0) = 1 + f(0).
                          f(0): Condiția n!=0 este falsă, deci returnează 0.  
    ```
    - Acum calculam: 0 + 1 + 0 + 3 + 0
    - Raspuns corect: `B`
3. Rezolvare
    ```json
        cifrele se aleg în ordine crescătoare, iar o soluție se afișează imediat ce suma cifrelor devine 6 (chiar dacă se mai pot adăuga cifre).

        Primele soluții sunt:

        1023
        1032
        105
        1203
        123
        1230

        Deci a șasea soluție generată este: 1230
    ```
    - Raspuns corect: `A`
4. Rezolvare:
    ```json
        Un arbore cu 10 noduri are întotdeauna: (n-1) 10−1=9 muchii și nu conține cicluri.

        Dacă adăugăm o singură muchie între două noduri ale arborelui, se formează exact un ciclu elementar, deoarece între cele două noduri exista deja un drum unic în arbore.

        Noua muchie închide acel drum și creează un singur ciclu.
    ```
    - Raspuns corect: `B`
5. Rezolvare:
    ```json
    ```

### Subiectul II
1. 
2. 
3. 
### Subiectul III

1. Rezolvare
    ```c++
    ```

2. Rezolvare
    ```C++
        #include <iostream>
        #include <cstring>

        using namespace std;

        int main() {

            int n, k;
            cin >> k >> n;
            int matrice[n][n];
            for (int i =0; i < n; i++) {
                for (int j = 0; j < n; j++) {
                    if (i == j) {
                        matrice[i][j] = k * (i+1);
                    } else if (j > i) {
                        matrice[i][j] = (k * (i+1)) + (j-i);
                    } else {
                        matrice[i][j] = (k * (i+1)) - (i-j);
                    }
                }
            }

            for (int i =0; i < n; i++) {
                for (int j = 0; j < n; j++) {
                    cout << matrice[i][j] << " ";
                }
                cout << endl;
            }

            return 0;
        }
    ```

3. 
    - a
        ```json
        ```
    - b
        ```c++
        ```