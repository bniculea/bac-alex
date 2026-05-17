# Test recapitulare elemente de baza


## Enunturi:

1. Să se reconstruiască un număr natural prin parcurgerea sa de la stânga la dreapta (folosind o metodă matematică sau recursivă, nu șiruri de caractere), eliminând toate cifrele pare. Dacă nu mai rămâne nicio cifră, se afișează `-1`.
- Exemplu date de iesire: `357`

2. Se dă un număr natural `N`. Să se determine cifra care apare de cele mai multe ori în scrierea lui `N`. Dacă sunt mai multe cifre cu număr maxim de apariții, se va afișa cea mai mare dintre ele.
- Exemplu date de intrare: `4455222`
- Exemplu date de iesire: `2`


3. Se dă un șir de `N` numere naturale cu valori între $0$ și $99$. Să se folosească un vector de frecvență pentru a afișa elementele unice din șir în ordine descrescătoare a numărului lor de apariții.
- Exemplu date de intrare: `n = 7;  5 3 5 2 3 5 7`
- Exemplu date de iesire: `5 3 2 7`


4. Se da un fisier ce contine o lista de numere cuprinse intre 1 si 1000000. Scrie un program care citeste din fisierul "numere.in" o lista de numere si afiseaza pe ecran cel mai mare numar ce se poate obtine din cifrele tuturor numerelor.
- Exemplu date de intrare: `2434 232 121 90`
- Exemplu date de iesire: `94433222210`


5.  Se dă un șir de caractere ce conține cuvinte separate prin spații. Să se ordoneze alfabetic cuvintele din șir utilizând funcțiile `strcmp` și `strcpy`.
- Exemplu date de intrare: `bacalaureat informatica examen`
- Exemplu date de iesire: `bacalaureat examen informatica`


6. Se dau două șiruri de caractere de lungimi egale. Să se creeze un al treilea șir prin alternarea caracterelor celor două șiruri.
- Exemplu date de intrare: `abc\nxyz`
- Exemplu date de iesire: `axbycz`


7. Să se scrie un program care deschide fișierul bac.txt în modul adăugare (ios::app) și append-ează la sfârșitul acestuia media aritmetică a numerelor pare deja existente în fișier. Numerele din fișier se vor citi în prealabil prin re-deschiderea sau citirea cu ifstream.

Exemplu date de intrare: bac.txt: 
   ```json
      2 4 5 7
   ```

Exemplu date de iesire: bac.txt: 
   ```json
      2 4 5 7 4.5
   ```


8. Să se scrie o funcție recursivă `int sumaCifre(int n)` care întoarce suma cifrele unui număr primit ca parametru.
- Exemplu date de intrare: `12345`
- Exemplu date de iesire: `15`


Exercitiu 63:
9. Să se scrie o funcție recursivă care numără câte vocale conține un șir de caractere primit ca parametru. Prototipul: `int numaraVocale(char s[])`.
- Exemplu date de intrare: `informatica`
- Exemplu date de iesire: `5`


Exercitiu 71----
10. Se dă o matrice cu `N` linii și $M$ coloane. Să se determine elementul aflat la intersecția diagonalelor (dacă matricea este pătratică și `N` este impar). În caz contrar să se afișeze textul `INCOMPATIBIL`.

Exercitiu 75:---
11. Enunt: Se dă o matrice cu `N` linii și $M$ coloane. Să se construiască un vector care să conțină elementul minim de pe fiecare coloană a matricei.


Exercitiu 82:---
12. Să se definească o structură `Cerc` formată dintr-un `Punct` (centrul cercului) și o rază (număr real). Să se verifice dacă un punct primit de la tastatură se află în interiorul cercului.
- Exemplu date de intrare: `cerc: centru(0,0), raza=5\npunct: (3,3)`
- Exemplu date de iesire: `DA`


13. Care este numărul de subgrafuri ale unui graf neorientat cu `N` noduri? Calculați pentru $n=4$.


14. Se dă vectorul de tați al unui arbore cu rădăcină: `tati = [0, 1, 1, 2, 2]`. Cine este rădăcina arborelui și câți fii are nodul 1? (Indexarea nodurilor de la 1 la 5).


15. Scrieți un program care citește un text linie cu linie din fișierul date.in și scrie în fișierul date.out doar liniile care nu încep cu o vocală.