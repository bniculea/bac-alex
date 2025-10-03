# Sesiunea 10

## Agenda

- Rezolvare tema
- Continuare discutii/exercitii
- Tema pentru acasa


## Rezolvare tema

- Mai jos gasesti primele 10 exercitii rezolvate intr-un singur program cu tot cu exemple de apelare:
    ```c++
        #include <iostream>
        #include <fstream>

        using namespace std;

        void salut();
        int patrat(int n);
        float suma(float a, float b);
        int estePar(int n);
        void afiseazaCaracter(char c, int n);
        void schimba(int &a, int &b);
        void dubleaza(int &x);
        void citesteNumar(int &x);
        float medie(float a, float b, float c);
        int max3(int a, int b, int c);


        int main() {

            salut();
            cout << endl;
            cout << patrat(11) << endl;
            cout <<suma(11, 2) << endl;
            cout << estePar(11) << endl;
            cout << estePar(10) << endl;
            afiseazaCaracter('A', 10);
            cout << endl;
            int a = 5, b = 7;
            schimba(a, b);
            cout << a << " " << b << endl;
            cout << endl;
            int x = 13;
            dubleaza(x);
            cout << x << endl;
            citesteNumar(x);
            cout << x << endl;
            cout << medie(2,3,4) << endl;
            cout << max3(2,30,4) << endl;
            return 0;
        }

        void salut() {
            cout << "Salut, lume!";
        }

        int patrat(int n) {
            return n * n;
        }

        float suma(float a, float b) {
            return a + b;
        }

        int estePar(int n) {
            return n % 2 == 0;
        }

        void afiseazaCaracter(char c, int n) {
            for (int i = 0; i < n; i++) {
                cout << c;
            }
        }

        void schimba(int &a, int &b) {
            int aux = a;
            a = b;
            b = aux;
        }

        void dubleaza(int &x) {
            x = x * 2;
        }

        void citesteNumar(int &x) {
            cin >> x;
        }
        float medie(float a, float b, float c) {
            return (a + b + c) / 3.0f;
        }

        int max3(int a, int b, int c) {
            int max = a;
            if (b > max) {
                max = b;
            }
            if (c > max) {
                max = c;
            }
            return max;
        }
    ```

-  Mai jos gasesti rezolvarile pentru problemele: 11,12,12,14,15 care au de a face cu vectorii
    ```c++
        #include <iostream>
        #include <fstream>

        using namespace std;

        void citireVector(int v[], int n);
        void afisareVector(int v[], int n);
        int sumaVector(int v[], int n);
        int maximVector(int v[], int n);
        void sorteazaVector(int v[], int n);

        int main() {
            int numere[10];
            citireVector(numere, 10);
            afisareVector(numere, 10);
            cout << endl;
            cout <<"Suma este: " << sumaVector(numere, 10) << endl;
            cout <<"Maxim este: " << maximVector(numere, 10) << endl;
            sorteazaVector(numere, 10);
            cout << "Dupa sortare: " << endl;
            afisareVector(numere, 10);
            return 0;
        }

        void citireVector(int v[], int n) {
            for (int i = 0; i < n; i++) {
                cin >> v[i];
            }
        }

        void afisareVector(int v[], int n) {
            for (int i = 0; i < n; i++) {
                cout << v[i] << " ";
            }
        }

        int sumaVector(int v[], int n) {
            int suma  = 0;
            for (int i = 0; i < n; i++) {
                suma += v[i];
            }

            return suma;
        }

        int maximVector(int v[], int n) {
            int max = v[0];
            for (int i = 1; i < n; i++) {
                if (v[i] > max) {
                    max = v[i];
                }
            }
            return max;
        }

        void sorteazaVector(int v[], int n) {
            for (int i = 0; i < n; i++) {
                for (int j = 0; j < n-1; j++) {
                    if (v[j] > v[j+1]) {
                        int aux = v[j];
                        v[j] = v[j+1];
                        v[j+1] = aux;
                    }
                }
            }
        }
    ```
16. Rezolvare:
    ```c++
        #include <iostream>
        #include <fstream>

        using namespace std;

        struct Student { char nume[30]; float nota; };

        void citireStudent(Student &s);
        void afisareStudent(Student s);
        float medieStudenti(Student v[], int n);

        int main() {
            Student s;
            citireStudent(s);
            afisareStudent(s);

            // Student studenti[4];
            // for (int i = 0; i < 4; i++) {
            //     citireStudent(studenti[i]);
            // }
            // cout << medieStudenti(studenti, 4) << endl;

            return 0;
        }

        void citireStudent(Student &s) {
            cout << "Nume: "; cin >> s.nume;
            cout << "Nota: "; cin >> s.nota;
        }
        void afisareStudent(Student s) {
            cout << "Nume: " << s.nume << endl;
            cout << "Nota: " << s.nota << endl;
        }

        float medieStudenti(Student v[], int n) {
            float suma = 0.0;
            for (int i = 0; i < n; i++) {
                suma += v[i].nota;
            }
            return suma / n ;
        }
    ```

17. Rezolvare:
    ```c++
        #include <iostream>

        using namespace std;

        int eliminaImpare(int n);

        int main() {
            cout << eliminaImpare(1234567) << endl;
            cout << eliminaImpare(135) << endl;
            return 0;
        }

        int eliminaImpare(int n) {
            int rezultat = 0;
            int p = 1;
            while (n) {
                int ultimaCifra = n % 10;
                if (ultimaCifra % 2 == 0) {
                    rezultat = ultimaCifra * p + rezultat;
                    p = p * 10;
                }
                n = n/10;
            }
            return rezultat;
        }
    ```

18. Rezolvare:
    ```c++
         #include <iostream>
        using namespace std;

        int dubleazaImpare(int n);

        int main() {

            int n = 123456;

            cout << dubleazaImpare(n);

            return 0;
        }

        int dubleazaImpare(int n) {
            int rezultat = 0;
            int pozitie = 1;
            while (n > 0) {
                int ultimaCifra = n % 10;
                if (ultimaCifra % 2 == 1) {
                    ultimaCifra = (ultimaCifra * 2) % 10;
                }

                rezultat = ultimaCifra * pozitie + rezultat;
                pozitie = pozitie * 10;
                n = n/10;
            }

            return rezultat;
        }
    ```

19. Rezolvare
    ```c++
         #include <iostream>
        using namespace std;

        int impartireJetoane(int n);

        int main() {

            int n = 12;

            cout << impartireJetoane(n);

            return 0;
        }

        int impartireJetoane(int n) {
            int contor = 0;
            for (int i = 2; i <= n; i++) {
                if (n % i == 0) {
                    contor++;
                }
            }

            return contor;
        }
    ```

- 20. Rezolvare
    ```c++
        #include <iostream>
        using namespace std;

        int identice(int n);

        int main() {

            int n = 22221;

            cout << identice(n);

            return 0;
        }

        int identice(int n) {
            int egale = 1;
            int ultimaCifraInitiala = n % 10;
            n = n/10;
            while (n > 0) {
                int ultimaCifraCurenta = n % 10;
                if (ultimaCifraInitiala != ultimaCifraCurenta) {
                    egale = 0;
                    break;
                }
                n = n/10;
            }

            return egale;
        }
    ```
- 21. Rezolvare
    ```c++
        #include <iostream>
        using namespace std;

        void afisare(int x, int y, int k);

        int main() {

            int x = 11, y = 21, k = 4;
            
            afisare(x,y,k);

            return 0;
        }

        void afisare(int x, int y, int k) {
            int contorNumereAfisate = 1;
            for (int i = x; i <= y; i++) {
                cout << i << " ";
                if ( contorNumereAfisate == k || i == y) {
                    cout << "* ";
                    contorNumereAfisate = 0;
                }
                contorNumereAfisate++;
            }
        }
    ```
- 22. Rezolvare:
    ```c++
         #include <iostream>
        using namespace std;

        void dublare1(int &n);
        int main() {

            int n = 85412;
            dublare1(n);
            cout << n;
            return 0;
        }

        void dublare1(int &n) {
            int copieN = n;
            int primaCifra;
            int pozitie = 1;
            while(n > 0) {
                primaCifra = n % 10;
                pozitie = pozitie * 10;
                n = n/10;
            }

            n = primaCifra * pozitie + copieN;
        }
    ```

- 23. Rezolvare
    ```c++
        #include <iostream>
        using namespace std;

        void prefix(int n, int k, int &output);

        int main() {

            int n = 27594;
            int k = 3;
            int x;
            prefix(n, k, x);
            cout << x;
            return 0;
        }

        void prefix(int n, int k, int &output) {
            int rezultat = 0;
            int pozitie = 1;

            while (pozitie * 10 <= n) {
                pozitie = pozitie * 10;
            }

            for (int i = 0; i < k; i++) {
                int cifraCurenta = n / pozitie;
                rezultat = rezultat * 10 + cifraCurenta;

                n = n % pozitie;
                pozitie = pozitie / 10;
            }

            output = rezultat;
        }
    ```

24. Rezolvare
    ```c++
        #include <iostream>
        using namespace std;

        void numar(int n, int c, int &m);

        int main() {

            int n = 5500;
            int c = 5;
            int m;
            numar(n, c, m);
            cout << m;
            return 0;
        }

        void numar(int n, int c, int &m) {
            int rezultat =0;
            int areDiferiteDeC =0;
            int pozitie = 1;
            while (n > 0) {
                int ultimaCifra = n % 10;
                if (ultimaCifra != c) {
                    rezultat = ultimaCifra * pozitie + rezultat;
                    pozitie = pozitie * 10;
                    if (ultimaCifra != 0) {
                        areDiferiteDeC = 1;
                    }
                }
                n = n / 10;
            }

            if (!areDiferiteDeC) {
                m = -1;
            } else {
                m = rezultat;
            }
        }
    ```

- 25. Rezolvare
    ```c++
        #include <iostream>
        using namespace std;

        int suma(int n);

        int main() {

            int n = 12345;
            cout << suma(n);

            return 0;
        }

        int suma(int n) {
            if (n == 0) {
                return 0;
            } else {
                int ultimaCifra = n % 10;
                return ultimaCifra + suma(n/10);
            }
        }
    ```

- 26. Rezolvare
    ```c++
        #include <iostream>
        using namespace std;

        void cmmdc(int a, int b, int& r);

        int main() {

            int a = 24;
            int b = 18;
            int rezultat;
            cmmdc(a, b, rezultat);

            cout << rezultat;

            return 0;
        }

        void cmmdc(int a, int b, int& r) {
            if (b == 0){
                r = a;
                return;
            }
            int reminder = a % b;
            cmmdc(b,  reminder, r);
        }
    ```
## Continuare discutii/exercitii
- Aici reluam ce nu am terminat sesiunea trecuta


## Tema

- Saptamana viitoare nu o sa putem face insa deoarece am acoperit o buna parte din materialul pentru bac vreau sa te uiti peste tot ce am facut si sa pui intrebari cu ce nu ai inteles.
- De exemplu gandeste-te ce nu stapanesti din:
    - Vectori
    - Matrici
    - Functii cu siruri:
        - strcpy, strncpy,strcat,strncat,strncmp,strcmp,strtok
    - Subprograme:
        - Recursive
        - Care intorc prin parametri
        - Care modifica parametri
    - etc
- Asta nu inseamna ca nu ai nimic de facut, daca nu ai intrebari efectiv nu tinem sesiunea, acum e randul tau sa pui intrebari.