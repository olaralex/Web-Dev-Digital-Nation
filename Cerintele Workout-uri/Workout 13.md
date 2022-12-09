# 13. WordPress

1. Instalează și activează plugin-ul *Advanced Custom Fields*
2. Din panoul de administrare, în bara din stânga accesează meniul *Custom Fields* și adaugă un nou Field Group. 
3. Pentru automatizarea zonei de caracteristici de pe Front Page:
    1. Adaugă un câmp de tip *Imagine*, pentru prima imagine dintre cele 3 coloane. Un câmp de tip *Text*, pentru titlu. Un câmp de tip *Textarea* pentru descriere. 
    2. Multiplică aceste câmpuri ca să obții câte 3 câmpuri pentru fiecare, deoarece pe home page avem 3 coloane cu câte o imagine, titlu și descriere în fiecare coloană.
    3. În secțiunea *Location* selectează *Page type is equal to Front Page*. În acest caz câmpurile vor apărea doar pentru pagina principală a site-ului.
    4. Salvează și publică aceste câmpuri. Deschide panoul de editare a Front Page-ului și completează spațiile cu imaginile și cu textele necesare.
    5. Pe site, în loc de imaginea introdusă direct în cod și în loc de textele scrise direct în codul paginii, înlocuiește cu apelarea funcției care să afișeze valoarea câmpului din panoul de administrare: `<?php the_field("CHEIA_CAMPULUI"); ?>`.
4. În același Field Group de mai devreme adaugă încă 3 câmpuri de tip *Number*, pentru acele 3 numere afișate pe Front Page, la secțiunea de *număr participanți la modulul X*. 
5. Din panoul de administrare completează câmpurile pentru acele numere iar, în codul paginii, înlocuiește valoarea cu funcția de returnare a câmpului tău nou creat. De exemplu: `$primul_numar = get_field("CHEIA_CAMPULUI");`.
*Atenție: Numărul din ultima coloană se calculează automat, ca sumă a primelor 3 numere, așa cum se întâmpla și până acum. Ultimul număr nu trebuiește setat din panoul de administrare.*