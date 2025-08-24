# Exercitii elementare Vectori

## Nota

- Exercitiile de mai jos au rolul de a te familiariza cu conceptul de vectori.
- Pentru fiecare exercitiu ai ca si exemplu un set de date intrare si cum ar trebui sa arate datele de iesire.
- Recomand a nu se folosi niciun instrument extern pentru rezolvarea lor
    - Aici ma refer sa nu cauti direct rezolvarea pe internet.
    - In cel mai rau caz, ce poti face, incearca sa faci cat cunosti si pe urma poti sa ii dai programul la chat gpt sa il intrebi ce ai gresit, dar nu sa iti dea direct rezolvarea, caci asa nu castigi nimic.
- Programelele sunt simple dar foarte utile. 
- Este important sa le rezolvi dar si mai important este sa le intelegi.
- Aminteste-ti sa eviti declararea de variabile numite cu o singura litera (exceptie desigur in cazul for-ului)
- Inainte de a incepe o problema, sparge-o in bucati si incepe sa rezolvi partea/partile pe care o cunosti, dupa care o sa vezi ca problema va deveni mai simpla
- Nu te arunca la rezolvare, incearca mai intai sa vezi ce ti se cere si acorda atentie exemplului, jumatate din problema e acolo.
- Spor la munca.

## Set de 20 de exerciții simple cu vectori

1. **Citirea și afișarea elementelor**  
   - **Enunț:** Se citește un număr natural `n` și apoi `n` numere întregi. Afișați toate numerele în ordinea în care au fost citite.  
   - **Date de intrare:**  
     ```
     5
     2 8 1 4 7
     ```  
   - **Date de ieșire:**  
     ```
     2 8 1 4 7
     ```

2. **Afișarea inversă**  
   - **Enunț:** Se citește un vector cu `n` numere întregi. Afișați elementele în ordine inversă.  
   - **Date de intrare:**  
     ```
     4
     10 20 30 40
     ```  
   - **Date de ieșire:**  
     ```
     40 30 20 10
     ```

3. **Numărarea elementelor pozitive**  
   - **Enunț:** Se citește un vector de `n` numere întregi. Determinați câte elemente sunt strict pozitive.  
   - **Date de intrare:**  
     ```
     6
     -3 7 0 5 -1 8
     ```  
   - **Date de ieșire:**  
     ```
     3
     ```

4. **Suma elementelor**  
   - **Enunț:** Se citește un vector de `n` numere întregi. Calculați suma elementelor.  
   - **Date de intrare:**  
     ```
     5
     1 2 3 4 5
     ```  
   - **Date de ieșire:**  
     ```
     15
     ```

5. **Media aritmetică**  
   - **Enunț:** Se citește un vector de `n` numere reale. Calculați media lor aritmetică.  
   - **Date de intrare:**  
     ```
     4
     2.0 4.0 6.0 8.0
     ```  
   - **Date de ieșire:**  
     ```
     5.00
     ```

6. **Valoarea maximă**  
   - **Enunț:** Se citește un vector de `n` numere întregi. Determinați valoarea maximă.  
   - **Date de intrare:**  
     ```
     5
     3 9 1 4 7
     ```  
   - **Date de ieșire:**  
     ```
     9
     ```

7. **Valoarea minimă și poziția**  
   - **Enunț:** Se citește un vector de `n` numere întregi. Afișați valoarea minimă și poziția (indexul) acesteia.  
   - **Date de intrare:**  
     ```
     5
     4 2 8 1 6
     ```  
   - **Date de ieșire:**  
     ```
     1 3
     ```

8. **Căutare element**  
   - **Enunț:** Se citește un vector și un număr `x`. Determinați dacă `x` apare în vector si afisati pozitia pe care se gaseste. In caz contrar afisati "nu exista"
   - **Date de intrare:**  
     ```
     5
     2 4 6 8 10
     6
     ```  
   - **Date de ieșire:**  
     ```
     2
     ```

9. **Numărarea aparițiilor**  
   - **Enunț:** Se citește un vector și un număr `x`. Afișați de câte ori apare `x` în vector.  
   - **Date de intrare:**  
     ```
     6
     1 2 3 2 2 4
     2
     ```  
   - **Date de ieșire:**  
     ```
     3
     ```

10. **Înlocuirea valorilor negative cu zero**  
    - **Enunț:** Se citește un vector. Înlocuiți toate valorile negative cu `0` și afișați vectorul modificat.  
    - **Date de intrare:**  
      ```
      5
      -3 4 -1 7 0
      ```  
    - **Date de ieșire:**  
      ```
      0 4 0 7 0
      ```

11. **Adunarea unei constante**  
    - **Enunț:** Se citește un vector și o valoare `k`. Adăugați `k` fiecărui element și afișați vectorul rezultat.  
    - **Date de intrare:**  
      ```
      4
      1 2 3 4
      5
      ```  
    - **Date de ieșire:**  
      ```
      6 7 8 9
      ```

12. **Afișarea elementelor pare**  
    - **Enunț:** Se citește un vector. Afișați toate elementele pare.  
    - **Date de intrare:**  
      ```
      6
      1 2 3 4 5 6
      ```  
    - **Date de ieșire:**  
      ```
      2 4 6
      ```

13. **Afișarea elementelor de pe poziții impare**  
    - **Enunț:** Se citește un vector. Afișați elementele aflate pe poziții impare (indexare de la 1).  
    - **Date de intrare:**  
      ```
      5
      10 20 30 40 50
      ```  
    - **Date de ieșire:**  
      ```
      10 30 50
      ```

14. **Sortare crescătoare**  
    - **Enunț:** Se citește un vector. Afișați elementele în ordine crescătoare.  
    - **Date de intrare:**  
      ```
      5
      3 1 4 2 5
      ```  
    - **Date de ieșire:**  
      ```
      1 2 3 4 5
      ```

15. **Sortare descrescătoare**  
    - **Enunț:** Se citește un vector. Afișați elementele în ordine descrescătoare.  
    - **Date de intrare:**  
      ```
      4
      10 40 30 20
      ```  
    - **Date de ieșire:**  
      ```
      40 30 20 10
      ```

16. **Suma numerelor pare**  
    - **Enunț:** Se citește un vector. Calculați suma numerelor pare din vector.  
    - **Date de intrare:**  
      ```
      5
      1 2 3 4 5
      ```  
    - **Date de ieșire:**  
      ```
      6
      ```

17. **Produsul numerelor nenule**  
    - **Enunț:** Se citește un vector. Calculați produsul numerelor nenule.  
    - **Date de intrare:**  
      ```
      4
      1 2 0 3
      ```  
    - **Date de ieșire:**  
      ```
      6
      ```

18. **Numere mai mari decât media**  
    - **Enunț:** Se citește un vector. Determinați câte elemente sunt mai mari decât media aritmetică a elementelor.  
    - **Date de intrare:**  
      ```
      5
      2 4 6 8 10
      ```  
    - **Date de ieșire:**  
      ```
      2
      ```

19. **Eliminarea unui element dat**  
    - **Enunț:** Se citește un vector și un număr `x`. Eliminați din vector toate aparițiile lui `x`.  
    - **Date de intrare:**  
      ```
      6
      1 2 3 2 4 2
      2
      ```  
    - **Date de ieșire:**  
      ```
      1 3 4
      ```

20. **Verificare ordine crescătoare**  
    - **Enunț:** Se citește un vector. Determinați dacă este ordonat crescător.  
    - **Date de intrare:**  
      ```
      4
      1 2 2 5
      ```  
    - **Date de ieșire:**  
      ```
      DA
      ```
