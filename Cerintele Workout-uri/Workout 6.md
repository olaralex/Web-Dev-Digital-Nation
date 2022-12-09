# 6. PHP

## Introducere

Există situații când avem nevoie să efectuăm niște calcule în pagină, să modificăm dinamic un fragment de text pe care l-am primit dintr-o bază de date sau dintr-o sursă pe care nu o putem controla și respectiv nu putem modifica acest text manual. 

HTML nu ne permite să facem acest lucru. În ajutor ne vine PHP, acesta este un **limbaj de programare** care știe să proceseze diferite logici.

**Ca rezultat, PHP livrează o pagină HTML construită în urma tuturor proceselor logice. Browserul preia acel HTML și îl afișează utilizatorului.** 

**Atenție**: De acum înainte nu vom mai putea accesa fișierul prin dublu click pe el. Pentru a vedea rezultatul afișării a fișierului index.php, de exemplu, e nevoie să îl deschidem prin intermediul serverului local (programul Local by Flywheel). Pentru asta deschide programul, activează proiectul, apasă pe butonul de vizualizare site iar în link-ul de browser adaugă calea spre fișier, relativ la site-ul tău, de exemplu: `nume-site.local/demo/index.php`

## Sarcini

1. Migrăm fișierele la PHP: Toate fișierele din proiect cu extensia `.html` le vom transforma în `.php`. 
2. În bara de navigare, din toate 3 fișiere, nu uita să corectezi link-urile ce duc spre celelalte pagini, de exemplu din `contact.html` să schimbi în `contact.php`.
3. Pe pagina principală (în fișierul index.php), înainte de footer adaugă o secțiune nouă împărțită în 4 coloane. 
4. Pe ecrane mici și până la "md" inclusiv acestea să se afișeaze în câte 2 coloane. 
5. Fiecare coloană va avea un număr, scris într-un div cu tag-ul `h3`, iar mai jos un text explicativ. Toate alineate pe centru. Unele dintre numere, nu neapărat toate, să fie mai mari de o mie (vom avea nevoie de numere mari pentru tema următoare).
6. Folosind variabile PHP, definește câte o variabilă pentru fiecare dintre numere. Atrebuie variabilei acel număr și apoi afișează în fiecare dintre primele 3 coloane valoarea variabilei corespunzătoare. Adică pentru prima coloană creezi o variabilă cu valoarea numărului și o afișezi cu `echo` sau `print` în tag-ul `h3`. Așa pentru fiecare coloană. 
7. În ultima coloană afișează suma tuturor celor 3 variabile. *A patra coloană reprezintă numărul total de participanți, primele 3 coloane reprezintă numărul de participanți la diferite module predate în cadrul "cursului revoluționar" pe care îl promovează pagina.*
8. Textul explicativ din primele 3 coloane vor avea următoarea formulare: "participanți la modulul X", unde X va primi numărul de la 1 la 3.
9. Definește o variabilă de PHP înainte de toate aceste coloane. La afișarea în fiecare coloană incrementeaz-o, astfel încât în prima coloană să fie cifra 1, în a doua cifra 2 și în a treia cifra 3. 
**ATENȚIE**: Nu scrie de mână aceste cifre, scopul este să exersăm incrementarea unei variabile de PHP. 
10. Definește o variabilă care să conțină șirul de caractere "participanți la modulul" (fără cifră). În fiecare coloană afișează acest text concatenat cu cifra generată de variablă. 
**ATENȚIE**: Vei avea un singur `echo` sau `print` care ar trebui să afișeze ambele variabile conactenate cu ajutorul operatorului de concatenare.