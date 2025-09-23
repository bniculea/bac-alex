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

## Exercitii functii / subprogramae