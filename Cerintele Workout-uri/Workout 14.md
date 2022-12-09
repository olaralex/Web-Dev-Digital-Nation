# 14. WordPress

1. Social Icons:
    1. Instalează și activează Plugin-ul *Easy Social Icons*.
    2. Adaugă câteva iconițe a rețelelor de socializare (în câmpul link-ului introduci # ca umplutură, pentru că nu avem încă link-uri reale).
    3. În fișierul `footer.php` din Child Theme găsește zona de copyright. Modifică structura în așa fel ca să ai 2 coloane. În prima coloană va rămâne textul de copyright, în a doua coloană vom afișa, alineate pe dreapta, simetric cu textul de copyright, iconițele de social media.
    4. Introdu shortcode-ul generat de plugin pentru a afișa iconițele.
    5. Pe ecranele mai mici, sub breakpoint-ul MD, afișează textul de copyright și iconițele unele sub celelalte alineate pe centru (*pentru alinierea textelor pe centru sau pe stânga/dreapta te poți folosi de clase Bootstrap cu breakpoint-uri, le găsești în documentație)*.
2. PopUp:
    1. Instalează și activează Plugin-ul *Hustle* sau *Popup Maker*.
    2. Creează un PopUp, te poți folosi de un template din colecție.
    3. Setează afișarea acestui PopUp pe site, cu întârziere de 10 secunde, o singură dată pentru un utilizator.
    4. În corpul PopUp-ului vei cere utilizatorului să se aboneze la newsletter și vei afișa același formular de abonare newsletter pe care l-ai folosit în footer-ul site-ului.
3. Site-ul în limba Română:
    1. Pentru început, să zicem că vrem ca site-ul să fie indexat de către Google ca site în limba Română și să apară în rezultatele căutării pentru căutări în Română. Pentru asta, din *Panoul de administrare -> Settings -> General -> Site Language* schimbă limba site-ului pe Română.
    *Notă: Dacă tot panoul de administrare a fost tradus în limba Română și tu vrei în continuare să îl vezi în limba engleză (doar site-ul pentru vizitatori să fie în Română), intră în Panoul de administrare -> Users -> Profile -> Language și setează Engleza pentru interfața panoului de administrare.*
    2. Observăm pe site, în mai multe locuri, texte care au rămas în limba Engleză (cel mai bine se vede în pagina de Blog, unde scrie: Read more, Posted on, etc.). Vom traduce aceste texte fără să le modificăm direct în cod.
    3. Instalează și activează Plugin-ul *Loco Translate*. 
    4. Găsește în interfața acestuia string-urile în limba Engleză care apar pe site și completează-le cu varianta în limba Română.
    5. Verifică pe site dacă s-a aplicat traducerea.
4. Pagina *Galerie Foto*.
    1. Instalează și activează Plugin-ul *Visual Portfolio, Posts & Image Gallery*.
    2. Creează o pagină nouă cu titlul *Galerie Foto*.
    3. Setează-i *Page Template* cu valoarea *Full Width*.
    4. Adaugă o galerie foto cu mai multe imagini (alege o variantă de stilizare potrivită pentru tine, în funcție de dimensiunile imaginilor). 
    5. Personalizează titlurile imaginilor pentru ca acestea să arate bine și să nu repete denumirea fișierului.