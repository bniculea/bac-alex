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
## Continuare discutii/exercitii

