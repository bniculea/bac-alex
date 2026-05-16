### Algoritmică de bază și numere (Exercițiile 1 - 15)

Exercitiu 1:
- Enunt: Se dă un număr natural $N$. Să se determine dacă acesta este prim. În caz afirmativ se va afișa `DA`, iar în caz contrar cel mai mare divizor propriu al său, sau `1` dacă nu are divizori proprii.
- Exemplu date de intrare: `27`
- Exemplu date de iesire: `9`

Exercitiu 2:
- Enunt: Să se scrie un program care citește un număr natural $N$ și afișează numărul de divizori improprii și numărul de divizori proprii ai săi, separați prin spațiu.
- Exemplu date de intrare: `12`
- Exemplu date de iesire: `2 4`

Exercitiu 3:
- Enunt: Se dă un număr natural $N$. Să se determine cifra maximă a numărului parcurgându-l cifră cu cifră de la dreapta la stânga și poziția ei (considerând prima cifră de la dreapta ca fiind pe poziția 1). Dacă cifra maximă apare de mai multe ori, se va lua poziția ei cea mai din stânga.
- Exemplu date de intrare: `58482`
- Exemplu date de iesire: `8 4`

Exercitiu 4:
- Enunt: Să se reconstruiască un număr natural prin parcurgerea sa de la stânga la dreapta (folosind o metodă matematică sau recursivă, nu șiruri de caractere), eliminând toate cifrele pare. Dacă nu mai rămâne nicio cifră, se afișează `-1`.
- Exemplu date de intrare: `234567`
- Exemplu date de iesire: `357`

Exercitiu 5:
- Enunt: Se dă un număr natural $N$. Să se verifice dacă inversul (oglinditul) său este un număr prim. Se va afișa `DA` sau `NU`.
- Exemplu date de intrare: `13`
- Exemplu date de iesire: `DA`

Exercitiu 6:
- Enunt: Se dă un interval $[a, b]$. Să se determine câte numere palindrom din acest interval au proprietatea că suma cifrelor lor este tot un număr palindrom.
- Exemplu date de intrare: `10 100`
- Exemplu date de iesire: `9`

Exercitiu 7:
- Enunt: Să se determine descompunerea în factori primi a unui număr natural $N$. Se vor afișa factorii primi și puterile lor sub forma $p^k$, separați prin caractere spațiu.
- Exemplu date de intrare: `360`
- Exemplu date de iesire: `2^3 3^2 5^1`

Exercitiu 8:
- Enunt: Se dau $N$ numere naturale. Să se determine cel mai mare divizor comun (CMMDC) al tuturor celor $N$ numere folosind algoritmul lui Euclid prin scăderi repetate sau împărțiri.
- Exemplu date de intrare: `4\n24 36 60 84`
- Exemplu date de iesire: `12`

Exercitiu 9:
- Enunt: Se dau două numere naturale $A$ și $B$. Să se calculeze cel mai mic multiplu comun (CMMMC) al lor. Atenție la posibilitatea depășirii tipurilor de date standard în timpul înmulțirii.
- Exemplu date de intrare: `12 18`
- Exemplu date de iesire: `36`

Exercitiu 10:
- Enunt: Se dă un număr natural $N$. Să se afișeze cel mai mic număr palindrom, strict mai mare decât $N$.
- Exemplu date de intrare: `123`
- Exemplu date de iesire: `131`

Exercitiu 11:
- Enunt: Se dă un număr natural $N$. Să se determine dacă $N$ poate fi scris ca sumă de doi divizori proprii ai săi. Se afișează `DA` sau `NU`.
- Exemplu date de intrare: `12`
- Exemplu date de iesire: `DA`

Exercitiu 12:
- Enunt: Se dă un număr natural $N$. Să se determine cifra care apare de cele mai multe ori în scrierea lui $N$. Dacă sunt mai multe cifre cu număr maxim de apariții, se va afișa cea mai mare dintre ele.
- Exemplu date de intrare: `4455222`
- Exemplu date de iesire: `2`

Exercitiu 13:
- Enunt: Se dau două numere naturale $A$ și $B$. Să se verifice dacă ele sunt "prietene" (adică au același număr de divizori proprii). Se va afișa `DA` sau `NU`.
- Exemplu date de intrare: `6 8`
- Exemplu date de iesire: `DA`

Exercitiu 14:
- Enunt: Se dă un număr natural $N$. Să se determine cel mai mare factor prim din descompunerea lui $N$.
- Exemplu date de intrare: `84`
- Exemplu date de iesire: `7`

Exercitiu 15:
- Enunt: Se dă un număr natural $N$. Să se determine dacă inversul său are număr impar de divizori. Se afișează `DA` sau `NU`.
- Exemplu date de intrare: `41`
- Exemplu date de iesire: `DA`

---

### Vectori și Tablouri Unidimensionale (Exercițiile 16 - 30)

Exercitiu 16:
- Enunt: Se dă un vector cu $N$ elemente întregi. Să se sorteze crescător elementele de pe poziții pare și descrescător elementele de pe poziții impare (considerând indexarea de la 1 la $N$), utilizând algoritmul Bubblesort.
- Exemplu date de intrare: `5\n7 2 9 1 5`
- Exemplu date de iesire: `9 1 7 2 5`

Exercitiu 17:
- Enunt: Se dă un vector cu $N$ elemente întregi și o valoare $X$. Să se insereze valoarea $X$ după fiecare element prim din vector. Să se afișeze vectorul rezultat.
- Exemplu date de intrare: `4\n3 4 5 6\n99`
- Exemplu date de iesire: `3 99 4 5 99 6`

Exercitiu 18:
- Enunt: Se dă un vector cu $N$ elemente întregi. Să se șteargă din vector toate elementele care sunt palindromuri. Dacă vectorul devine gol, se va afișa `GOL`.
- Exemplu date de intrare: `4\n121 45 66 78`
- Exemplu date de iesire: `45 78`

Exercitiu 19:
- Enunt: Se dă un șir de $N$ numere naturale cu valori între $0$ și $99$. Să se folosească un vector de frecvență pentru a afișa elementele unice din șir în ordine descrescătoare a numărului lor de apariții.
- Exemplu date de intrare: `7\n5 3 5 2 3 5 7`
- Exemplu date de iesire: `5 3 2 7`

Exercitiu 20:
- Enunt: Se dă un vector cu $N$ elemente întregi ordonate crescător. Să se elimine duplicatele din vector fără a folosi un vector suplimentar și păstrând ordinea.
- Exemplu date de intrare: `6\n1 2 2 3 4 4`
- Exemplu date de iesire: `1 2 3 4`

Exercitiu 21:
- Enunt: Se dau doi vectori sortați crescător, cu $N$, respectiv $M$ elemente. Să se interclaseze cei doi vectori într-un al treilea vector, eliminând în același timp elementele communes.
- Exemplu date de intrare: `3\n1 3 5\n3\n2 3 6`
- Exemplu date de iesire: `1 2 5 6`

Exercitiu 22:
- Enunt: Se dă un vector cu $N$ elemente întregi. Să se determine lungimea maximă a unei secvențe de elemente cu semne alternante (pozitiv, negativ, pozitiv etc.).
- Exemplu date de intrare: `5\n1 -2 3 4 -5`
- Exemplu date de iesire: `3`

Exercitiu 23:
- Enunt: Se dă un vector de frecvență ce conține cifrele unui număr mare. Să se afișeze cel mai mare număr care se poate forma cu aceste cifre.
- Exemplu date de intrare: `frecventa: ap[2]=2, ap[5]=1, ap[9]=2`
- Exemplu date de iesire: `99522`

Exercitiu 24:
- Enunt: Se dă un vector cu $N$ elemente. Să se insereze pe poziția $K$ (indexată de la 1) media aritmetică a elementelor de dinainte de $K$.
- Exemplu date de intrare: `4 3\n2 4 6 8`
- Exemplu date de iesire: `2 4 3 6 8`

Exercitiu 25:
- Enunt: Se dă un vector cu $N$ numere naturale. Să se determine dacă vectorul poate fi împărțit în două secvențe disjuncte care să aibă sume egale. Se afișează indicele de tăiere sau `NU`.
- Exemplu date de intrare: `4\n1 2 3 6`
- Exemplu date de iesire: `3`

Exercitiu 26:
- Enunt: Se dă un vector cu $N$ elemente întregi. Să se permute circular elementele vectorului cu o poziție spre stânga.
- Exemplu date de intrare: `4\n10 20 30 40`
- Exemplu date de iesire: `20 30 40 10`

Exercitiu 27:
- Enunt: Se dă un vector cu $N$ elemente. Să se verifice dacă elementele vectorului formează o progresie aritmetică. Să se afișeze rația progresiei sau `NU`.
- Exemplu date de intrare: `4\n2 5 8 11`
- Exemplu date de iesire: `3`

Exercitiu 28:
- Enunt: Se dă un vector cu $N$ elemente. Să se șteargă elementul de pe poziția minimului din vector. Dacă sunt mai multe elemente cu valoare minimă, se va șterge primul.
- Exemplu date de intrare: `5\n4 2 7 2 9`
- Exemplu date de iesire: `4 7 2 9`

Exercitiu 29:
- Enunt: Se dă un vector cu $N$ numere naturale. Să se determine elementul majoritar din vector (elementul care apare de mai mult de $N/2$ ori). Dacă nu există, se afișează `-1`.
- Exemplu date de intrare: `5\n3 2 3 1 3`
- Exemplu date de iesire: `3`

Exercitiu 30:
- Enunt: Se dă un vector cu $N$ elemente. Să se ordoneze vectorul astfel încât toate valorile pare să apară la început, sortate crescător, urmate de cele impare, sortate descrescător.
- Exemplu date de intrare: `5\n3 2 8 5 1`
- Exemplu date de iesire: `2 8 5 3 1`

---

### Șiruri de caractere (Exercițiile 31 - 50)

Exercitiu 31:
- Enunt: Se dă un șir de caractere ce conține cuvinte separate prin spații. Să se ordoneze alfabetic cuvintele din șir utilizând funcțiile `strcmp` și `strcpy`.
- Exemplu date de intrare: `bacalaureat informatica examen`
- Exemplu date de iesire: `bacalaureat examen informatica`

Exercitiu 32:
- Enunt: Se dă un șir de caractere. Să se elimine din șir toate aparițiile unei vocale citite de la tastatură folosind funcția `strcpy`.
- Exemplu date de intrare: `informatica\na`
- Exemplu date de iesire: `informtic`

Exercitiu 33:
- Enunt: Se dau două șiruri de caractere $S_1$ și $S_2$. Să se verifice dacă $S_2$ este sufix al lui $S_1$ folosind funcțiile `strlen` și `strcmp` (sau `strncmp`). Se va afișa `DA` sau `NU`.
- Exemplu date de intrare: `programare\namare`
- Exemplu date de iesire: `DA`

Exercitiu 34:
- Enunt: Se dă un text format din cuvinte separate prin caracterele `;`, `_` sau spațiu. Să se folosească funcția `strtok` pentru a extrage cuvintele și să se afișeze doar cele care au lungime impară.
- Exemplu date de intrare: `Ana;are_mere mari`
- Exemplu date de iesire: `Ana\nmere`

Exercitiu 35:
- Enunt: Se dă un șir de caractere format din litere și cifre. Să se determine suma tuturor cifrelor care apar în text utilizând funcția `strchr` sau parcurgerea elementară și conversia din caracter în număr.
- Exemplu date de intrare: `a3b5_2`
- Exemplu date de iesire: `10`

Exercitiu 36:
- Enunt: Se dau două șiruri de caractere $S_1$ și $S_2$. Să se afișeze prima poziție din $S_1$ unde începe subșirul $S_2$, utilizând funcția `strstr`. Dacă subșirul nu există, se va afișa `-1`.
- Exemplu date de intrare: `antreprenor\ntre`
- Exemplu date de iesire: `2`

Exercitiu 37:
- Enunt: Se citește o matrice de cuvinte cu $N$ linii (fiecare linie conținând un cuvânt). Să se afișeze cuvântul din matrice care conține cele mai multe consoane.
- Exemplu date de intrare: `3\nana\nmere\nscris`
- Exemplu date de iesire: `scris`

Exercitiu 38:
- Enunt: Se dă un șir de caractere. Să se dubleze fiecare vocală din șir folosind mutări repetate de caractere sau `strcat`/`strcpy`.
- Exemplu date de intrare: `bac`
- Exemplu date de iesire: `baac`

Exercitiu 39:
- Enunt: Se dă un șir de caractere ce reprezintă un număr mare. Să se convertească fiecare caracter-cifră în valoarea sa numerică efectivă și să se verifice dacă numărul reprezentat este divizibil cu 3.
- Exemplu date de intrare: `126`
- Exemplu date de iesire: `DA`

Exercitiu 40:
- Enunt: Se dă un text. Să se determine numărul de cuvinte care încep și se termină cu aceeași literă. Cuvintele sunt separate prin spațiu.
- Exemplu date de intrare: `capacul are un text bun`
- Exemplu date de iesire: `2`

Exercitiu 41:
- Enunt: Se dă un șir de caractere. Să se determine câte dintre caracterele din șir sunt litere mari ale alfabetului, folosind funcții din biblioteca `<cctype>` (de exemplu `isupper`).
- Exemplu date de intrare: `InfoBac2026`
- Exemplu date de iesire: `2`

Exercitiu 42:
- Enunt: Se dau două șiruri de caractere de lungimi egale. Să se creeze un al treilea șir prin alternarea caracterelor celor două șiruri.
- Exemplu date de intrare: `abc\nxyz`
- Exemplu date de iesire: `axbycz`

Exercitiu 43:
- Enunt: Se dă un șir de caractere format din cuvinte separate prin spațiu. Să se înlocuiască prima literă a fiecărui cuvânt cu litera mare corespunzătoare.
- Exemplu date de intrare: `examen de bacalaureat`
- Exemplu date de iesire: `Examen De Bacalaureat`

Exercitiu 44:
- Enunt: Se dă un șir de caractere. Să se verifice dacă șirul este un palindrom din punct de vedere al caracterelor (ignorând spațiile).
- Exemplu date de intrare: `rezerver`
- Exemplu date de iesire: `DA`

Exercitiu 45:
- Enunt: Se dă un text format din cuvinte separate prin spațiu. Să se afișeze textul în care s-a inversat ordinea cuvintelor (fără a inversa literele din interiorul cuvintelor).
- Exemplu date de intrare: `vine vacanta de vara`
- Exemplu date de iesire: `vara de vacanta vine`

Exercitiu 46:
- Enunt: Se dă un șir de caractere. Să se verifice dacă conține doar caractere numerice. Se va afișa `DA` sau `NU`.
- Exemplu date de intrare: `123a45`
- Exemplu date de iesire: `NU`

Exercitiu 47:
- Enunt: Se dă un șir de caractere. Să se comprime șirul înlocuind secvențele de caractere identice cu caracterul respectiv urmat de numărul de apariții.
- Exemplu date de intrare: `aaabbc`
- Exemplu date de iesire: `a3b2c1`

Exercitiu 48:
- Enunt: Se dă o matrice de cuvinte. Să se sorteze liniile matricei crescător în funcție de lungimea cuvintelor stocate pe fiecare linie.
- Exemplu date de intrare: `3\nelefant\nana\nmere`
- Exemplu date de iesire: `ana\nmere\nelefant`

Exercitiu 49:
- Enunt: Se dau două șiruri de caractere. Să se concateneze primele $K$ caractere din al doilea șir la sfârșitul primului șir, utilizând funcția `strncat`.
- Exemplu date de intrare: `baza\ntextul_nou 4`
- Exemplu date de iesire: `bazatext`

Exercitiu 50:
- Enunt: Se dă un text. Să se șteargă toate spațiile multiple dintre cuvinte, astfel încât să rămână un singur spațiu ca separator.
- Exemplu date de intrare: `Informatica    este   frumoasa`
- Exemplu date de iesire: `Informatica este frumoasa`

---

### Funcții / Subprograme și Recursivitate (Exercițiile 51 - 65)

Exercitiu 51:
- Enunt: Să se definească un subprogram cu prototipul `int sumaDivizori(int n)` care returnează suma divizorilor proprii ai lui `n`. În `main` se va efectua apelul pentru a determina toate numerele perfecte mai mici decât un $X$ dat (un număr e perfect dacă e egal cu suma divizorilor săi proprii plus 1).
- Exemplu date de intrare: `10`
- Exemplu date de iesire: `6`

Exercitiu 52:
- Enunt: Să se scrie o funcție `void modificaVector(int arr[], int n)` care modifică vectorul primit ca parametru, înlocuind fiecare element cu numărul său de divizori. Funcția nu întoarce o valoare direct, ci prin intermediul vectorului.
- Exemplu date de intrare: `3\n4 5 6`
- Exemplu date de iesire: `3 2 4`

Exercitiu 53:
- Enunt: Să se scrie un subprogram cu prototipul `void oglindit(int n, int &val)` care primește prin `n` un număr natural și returnează prin parametrul transmis prin referință `val` oglinditul lui `n`.
- Exemplu date de intrare: `5432`
- Exemplu date de iesire: `2345`

Exercitiu 54:
- Enunt: Explicați printr-un comentariu diferența dintre prototipul (declararea) unei funcții și definirea acesteia. Scrieți un program care definește o funcție recursivă `int cmmdc_rec(int a, int b)` bazată pe algoritmul lui Euclid și o apelează în `main`.
- Exemplu date de intrare: `14 21`
- Exemplu date de iesire: `7`

Exercitiu 55:
- Enunt: Să se scrie o funcție recursivă `int sumaCifre(int n)` care întoarce suma cifrele unui număr primit ca parametru.
- Exemplu date de intrare: `12345`
- Exemplu date de iesire: `15`

Exercitiu 56:
- Enunt: Să se scrie un subprogram recursiv cu prototipul `void cifreMari(int n, int &maxi)` care determină prin parametrul transmis prin referință `maxi` cifra maximă dintr-un număr natural $N$.
- Exemplu date de intrare: `4731`
- Exemplu date de iesire: `7`

Exercitiu 57:
- Enunt: Scrieți o funcție recursivă `int factorial(int n)` și folosiți-o pentru a calcula combinări de $N$ luate câte $K$ ($C_n^k = \frac{n!}{k!(n-k)!}$).
- Exemplu date de intrare: `5 2`
- Exemplu date de iesire: `10`

Exercitiu 58:
- Enunt: Să se scrie o funcție recursivă cu prototipul `int fibonacci(int n)` care returnează al $N$-lea termen din șirul Fibonacci ($1, 1, 2, 3, 5, 8...$).
- Exemplu date de intrare: `6`
- Exemplu date de iesire: `8`

Exercitiu 59:
- Enunt: Să se scrie o funcție `bool ePrim(int n)` care verifică dacă un număr este prim. Să se folosească această funcție pentru a scrie o altă funcție `void urmatorulPrim(int n, int &p)` care returnează prin referință cel mai mic număr prim strict mai mare decât $N$.
- Exemplu date de intrare: `8`
- Exemplu date de iesire: `11`

Exercitiu 60:
- Enunt: Să se realizeze o funcție recursivă `void afisareBaza2(int n)` care afișează reprezentarea în baza 2 a unui număr natural $N$.
- Exemplu date de intrare: `13`
- Exemplu date de iesire: `1101`

Exercitiu 61:
- Enunt: Să se scrie o funcție recursivă care primește ca parametru un vector și dimensiunea sa și returnează valoarea maximă din vector. Prototipul: `int maxVector(int v[], int n)`.
- Exemplu date de intrare: `4\n12 45 67 2`
- Exemplu date de iesire: `67`

Exercitiu 62:
- Enunt: Să se scrie o funcție `void stergePozitie(int v[], int &n, int poz)` care elimină elementul de pe poziția `poz` dintr-un vector cu `n` elemente, modificând valoarea lui `n` prin referință.
- Exemplu date de intrare: `4\n10 20 30 40\n2`
- Exemplu date de iesire: `10 30 40` (iar n devine 3)

Exercitiu 63:
- Enunt: Să se scrie o funcție recursivă care numără câte vocale conține un șir de caractere primit ca parametru. Prototipul: `int numaraVocale(char s[])`.
- Exemplu date de intrare: `informatica`
- Exemplu date de iesire: `5`

Exercitiu 64:
- Enunt: Să se scrie un subprogram recursiv care primește ca parametru un număr natural $N$ și returnează numărul format doar din cifrele sale impare. Dacă nu conține cifre impare, returnează 0.
- Exemplu date de intrare: `23456`
- Exemplu date de iesire: `35`

Exercitiu 65:
- Enunt: Să se scrie o funcție `void simplificareFractie(int &a, int &b)` care primește numărătorul `a` și numitorul `b` ai unei fracții și îi modifică prin referință astfel încât fracția să devină ireductibilă (folosind CMMDC).
- Exemplu date de intrare: `12 18`
- Exemplu date de iesire: `2 3`

---

### Matrici / Tablouri Bidimensionale (Exercițiile 66 - 75)

Exercitiu 66:
- Enunt: Se dă o matrice pătratică de dimensiune $N \times N$. Să se calculeze suma elementelor aflate pe diagonala principală și produsul elementelor de pe diagonala secundară.
- Exemplu date de intrare: `3\n1 2 3\n4 5 6\n7 8 9`
- Exemplu date de iesire: `Suma=15 Produs=105`

Exercitiu 67:
- Enunt: Se dă o matrice pătratică de dimensiune $N \times N$. Să se determine maximul din zona de Nord (strict deasupra diagonalei principale și deasupra diagonalei secundare).
- Exemplu date de intrare: `3\n1 9 3\n4 5 6\n7 8 9`
- Exemplu date de iesire: `9`

Exercitiu 68:
- Enunt: Se dă o matrice pătratică de dimensiune $N \times N$. Să se afișeze media aritmetică a elementelor situate în zona de Sud (strict sub diagonala principală și sub diagonala secundară).
- Exemplu date de intrare: `3\n1 2 3\n4 5 6\n7 10 9`
- Exemplu date de iesire: `10`

Exercitiu 69:
- Enunt: Se dă o matrice pătratică de dimensiune $N \times N$. Să se permute zona de Est cu zona de Vest (elementele delimitate strict de cele două diagonale).
- Exemplu date de intrare: `3\n1 2 3\n10 5 20\n7 8 9`
- Exemplu date de iesire: `1 2 3\n20 5 10\n7 8 9`

Exercitiu 70:
- Enunt: Se dă o matrice oarecare cu $N$ linii și $M$ coloane. Să se determine linia pe care suma elementelor este maximă. Dacă sunt mai multe linii, se afișează prima dintre ele.
- Exemplu date de intrare: `2 3\n1 2 3\n7 0 1`
- Exemplu date de iesire: `1`

Exercitiu 71:
- Enunt: Se dă o matrice cu $N$ linii și $M$ coloane. Să se determine elementul aflat la intersecția diagonalelor (dacă matricea este pătratică și $N$ este impar). În caz contrar să se afișeze textul `INCOMPATIBIL`.
- Exemplu date de intrare: `3\n1 2 3\n4 9 6\n7 8 9`
- Exemplu date de iesire: `9`

Exercitiu 72:
- Enunt: Se dă o matrice oarecare cu $N$ linii și $M$ coloane. Să se ordoneze crescător elementele de pe fiecare linie a matricei folosind un algoritm valid de sortare.
- Exemplu date de intrare: `2 3\n3 1 2\n9 5 7`
- Exemplu date de iesire: `1 2 3\n5 7 9`

Exercitiu 73:
- Enunt: Se dă o matrice pătratică de dimensiune $N \times N$. Să se determine dacă matricea este simetrică față de diagonala principală. Se va afișa `DA` sau `NU`.
- Exemplu date de intrare: `3\n1 2 3\n2 4 5\n3 5 6`
- Exemplu date de iesire: `DA`

Exercitiu 74:
- Enunt: Să se genereze o matrice cu $N$ linii și $N$ coloane în care elementele de pe diagonala principală sunt egale cu `1`, cele de pe diagonala secundară sunt egale cu `2`, intersecția lor (dacă există) este `3`, iar restul elementelor sunt `0`.
- Exemplu date de intrare: `3`
- Exemplu date de iesire: `1 0 2\n0 3 0\n2 0 1`

Exercitiu 75:
- Enunt: Se dă o matrice cu $N$ linii și $M$ coloane. Să se construiască un vector care să conțină elementul minim de pe fiecare coloană a matricei.
- Exemplu date de intrare: `3 3\n4 8 9\n1 5 12\n6 2 7`
- Exemplu date de iesire: `1 2 7`

---

### Structuri / Tipul struct (Exercițiile 76 - 83)

Exercitiu 76:
- Enunt: Să se definească o structură numită `Fractie` cu membrii `numarator` și `numitor` (numere întregi). Scrieți un program care citește două variabile de acest tip și afișează structura ce reprezintă suma lor, adusă la forma ireductibilă.
- Exemplu date de intrare: `1 2\n1 4` (reprezentând 1/2 și 1/4)
- Exemplu date de iesire: `3 4` (reprezentând 3/4)

Exercitiu 77:
- Enunt: Să se definească o structură `Elev` (nume - șir de caractere, medie - număr real). Să se citească un vector de structuri cu $N$ elevi și să se sorteze descrescător în funcție de medie. La medii egale, sortarea se va face alfabetic după nume.
- Exemplu date de intrare: `2\nPopescu 9.50\nIonescu 9.80`
- Exemplu date de iesire: `Ionescu 9.80\nPopescu 9.50`

Exercitiu 78:
- Enunt: Să se definească o structură `Punct` (coordonate `x` și `y` numere reale). Să se inițializeze două variabile de acest tip și să se calculeze distanța euclidiană dintre ele.
- Exemplu date de intrare: `0 0\n3 4`
- Exemplu date de iesire: `5`

Exercitiu 79:
- Enunt: Definiți o structură numită `Data` (zi, luna, an - întregi) și o structură `Eveniment` (nume - șir de caractere, data_ev - variabilă de tipul `Data`). Să se verifice dacă un eveniment are loc într-un an bisect.
- Exemplu date de intrare: `Concert\n15 5 2024`
- Exemplu date de iesire: `DA`

Exercitiu 80:
- Enunt: Se dă un vector de structuri de tip `Produs` (cod - întreg, pret - real, stoc - întreg). Să se afișeze valoarea totală a produselor din stoc (pret * stoc) pentru toate produsele care au stocul mai mic decât 10.
- Exemplu date de intrare: `2\n101 5.0 4\n102 10.0 15`
- Exemplu date de iesire: `20.0`

Exercitiu 81:
- Enunt: Se dă o structură `Complex` (re, im - numere reale). Să se scrie o funcție care primește două numere complexe ca parametru și returnează structura ce reprezintă produsul lor.
- Exemplu date de intrare: `1 2\n3 4` ( (1+2i)*(3+4i) )
- Exemplu date de iesire: `-5 10` ( -5 + 10i )

Exercitiu 82:
- Enunt: Să se definească o structură `Cerc` formată dintr-un `Punct` (centrul cercului) și o rază (număr real). Să se verifice dacă un punct primit de la tastatură se află în interiorul cercului.
- Exemplu date de intrare: `cerc: centru(0,0), raza=5\npunct: (3,3)`
- Exemplu date de iesire: `DA`

Exercitiu 83:
- Enunt: Se citește un vector de $N$ melodii stocate în structuri de tip `Melodie` (titlu, durata_secunde). Să se exprime durata totală a tuturor melodiilor în formatul `Ore:Minute:Secunde`.
- Exemplu date de intrare: `2\nMelodie1 120\nMelodie2 240`
- Exemplu date de iesire: `0:6:0`

---

### Teoria Grafurilor (Exercițiile 84 - 95)

Exercitiu 84:
- Enunt: Care este formula pentru numărul maxim de muchii într-un graf neorientat cu $n$ noduri fără bucle și muchii multiple? Calculați valoarea pentru $n=6$.
- Exemplu date de intrare: `6`
- Exemplu date de iesire: `15` (Formula: $n \times (n-1) / 2$)

Exercitiu 85:
- Enunt: Într-un graf neorientat, suma gradelor tuturor nodurilor este legată direct de numărul de muchii $m$. Care este această formulă teoretică? Determinați suma gradelor dacă graful are $12$ muchii.
- Exemplu date de intrare: `12`
- Exemplu date de iesire: `24` (Suma gradelor = $2 \times m$)

Exercitiu 86:
- Enunt: Folosind definițiile componentelor conexe: dacă un graf neorientat cu $n=8$ noduri are $3$ componente conexe, care este numărul maxim posibil de muchii pe care le poate avea acest graf?
- Exemplu date de intrare: `8 3`
- Exemplu date de iesire: `15` (Numărul maxim de muchii se obține când o componentă conține $n-c+1$ noduri, adică $8-3+1 = 6$ noduri, restul având câte 1 nod. $6 \times 5 / 2 = 15$)

Exercitiu 87:
- Enunt: Care este numărul total de grafuri parțiale posibile ale unui graf neorientat cu $m$ muchii? Calculați rezultatul pentru un graf cu $5$ muchii.
- Exemplu date de intrare: `5`
- Exemplu date de iesire: `32` (Formula: $2^m$)

Exercitiu 88:
- Enunt: Care este numărul de subgrafuri ale unui graf neorientat cu $n$ noduri? Calculați pentru $n=4$.
- Exemplu date de intrare: `4`
- Exemplu date de iesire: `15` (Formula pentru subgrafuri nevide: $2^n - 1$)

Exercitiu 89:
- Enunt: Definiți noțiunea de graf Hamiltonian și graf Eulerian. Un graf neorientat are gradele nodurilor: `2, 4, 2, 2, 2`. Este acesta cu siguranță un graf Eulerian? Răspundeți cu `DA` sau `NU` pe baza teoremei Euleriene (toate nodurile au grad par și graful e conex - presupunem conexitatea).
- Exemplu date de intrare: `2 4 2 2 2`
- Exemplu date de iesire: `DA`

Exercitiu 90:
- Enunt: Un arbore este un graf neorientat conex și aciclic. Câte muchii are un arbore cu $n=100$ noduri?
- Exemplu date de intrare: `100`
- Exemplu date de iesire: `99` (Formula: $n - 1$)

Exercitiu 91:
- Enunt: Într-un graf orientat, care este relația dintre suma gradelor exterioare ($d^+$), suma gradelor interioare ($d^-$) și numărul de arce $m$? Calculați suma gradelor exterioare dacă graful are $15$ arce.
- Exemplu date de intrare: `15`
- Exemplu date de iesire: `15` (Relație: $\sum d^+ = \sum d^- = m$)

Exercitiu 92:
- Enunt: Care este numărul maxim de arce dintr-un graf orientat cu $n$ noduri (fără bucle)? Calculați pentru $n=5$.
- Exemplu date de intrare: `5`
- Exemplu date de iesire: `20` (Formula: $n \times (n-1)$)

Exercitiu 93:
- Enunt: Definiți noțiunea de graf tare conex. Dacă o matrice de adiacență a unui graf orientat cu 3 noduri are toate elementele egale cu `1` (inclusiv pe diagonala principală), este graful tare conex? Răspundeți cu `DA` sau `NU`.
- Exemplu date de iesire: `DA`

Exercitiu 94:
- Enunt: Se dă vectorul de tați al unui arbore cu rădăcină: `tati = [0, 1, 1, 2, 2]`. Cine este rădăcina arborelui și câți fii are nodul 1? (Indexarea nodurilor de la 1 la 5).
- Exemplu date de intrare: `0 1 1 2 2`
- Exemplu date de iesire: `Radacina=1 Fii=2` (Nodurile 2 și 3 au tatăl 1)

Exercitiu 95:
- Enunt: Se dă o matrice de adiacență a unui graf neorientat. Să se determine gradul nodului $K$ primit de la tastatură (gradul este numărul de elemente de `1` de pe linia $K$).
- Exemplu date de intrare: `3 2\n0 1 1\n1 0 0\n1 0 0` (Matricea și K=2)
- Exemplu date de iesire: `1`


Exercitiu 96:

Enunt: Să se scrie un program care citește un șir necunoscut de numere întregi din fișierul numere.in. Să se determine și să se afișeze pe ecran cel mai mare număr citit și numărul său de apariții.

Exemplu date de intrare: numere.in: 5 8 3 8 4 8

Exemplu date de iesire: 8 3

Exercitiu 97:

Enunt: Scrieți un program care citește un text linie cu linie din fișierul date.in și scrie în fișierul date.out doar liniile care nu încep cu o vocală.

Exemplu date de intrare: date.in:\nana are mere\nmerele sunt bune

Exemplu date de iesire: date.out:\nmerele sunt bune


Exercitiu 98:

Enunt: Să se scrie un program care deschide fișierul bac.txt în modul adăugare (ios::app) și append-ează la sfârșitul acestuia media aritmetică a numerelor pare deja existente în fișier. Numerele din fișier se vor citi în prealabil prin re-deschiderea sau citirea cu ifstream.

Exemplu date de intrare: bac.txt: 
   ```json
      2 4 5 7
   ```

Exemplu date de iesire: bac.txt: 
   ```json
      2 4 5 7 4.5
   ```
---