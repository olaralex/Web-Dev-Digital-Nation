# 5. Bootstrap

1. Înainte de prezentarea generală (imediat după bara de navigare) adaugă un carousel pe toată lățimea ecranului (adică **nu** va fi îmbrăcat în clasa .container). Dacă vei adăuga în carousel imagini random de diferite mărimi, vei observa că, la schimbarea următorului slide din carousel, se schimbă înălțimea paginii, ceea ce este cam deranjant pentru vizitatori. Din acest motiv vom recurge la varianta de `background-image`, cu ajutorul căruia putem să manipulăm mai simplu imaginile:
    1. Exemplul de carousel din documentația Bootstrap are 3 imagini. Fragmentul de cod pentru fiecare arată în felul următor:
    `<img src="..." class="d-block w-100" alt="...">`
    Înlocuiește acest fragment de cod cu:
    `<div style="background-image: url(...);"></div>`
    Unde în loc de ... introduci link-ul spre niște imagini din internet (la alegerea ta). 
    2. În fișierul de stiluri indică imaginii de background să fie `cover` și să fie pozitionată pe centru. 
    3. Înălțimea fiecărui slide ar trebui să fie, de exemplu, 40% din lățimea acestuia (respectiv imaginile ar trebui să se taie de sus și de jos pentru a se poziționa bine în interiorul slide-ului).
2. Butoanele din zona de prezentare generală: 
În documentația Bootstrap găsește clasele potrivite pentru butoane și aplică-le pe acele două butoane afișate în pagină. De exemplu, primul buton fă-l de culoare albastră iar al doilea să fie de culoare gri (clasa Secondary) și să fie outline (doar cu border, fără culoare de fundal).
3. În banda de footer, la formularul de abonare newsletter vom aplica stiluri de Bootstrap pentru câmp și pentru buton:
    1. Din documentația Bootstrap, la secțiunea "Button group", găsește exemplul de cod în care este introdus și un input (input este câmpul de introducere a adresei de email). Reprodu aceeași structură pentru a avea câmpul și butonul într-un grup, la fel ca în exemplele din documentație (lipite între ele și cu colțurile opuse rotunjite).
    2. Adaugă clasele necesare atât input-ului cât și butonului (butonul să devină albastru, de exemplu). 
    3. După ce ai făcut totul corect, acest câmp ar trebui să se lungească pe toată lățimea ecranului. Noi nu ne dorim acest lucru, așa că recomand să îmbrăcăm tot acest input group într-un `.row` și într-o coloană, care să fie mai îngustă, de exemplu 1/3 pe ecranele mari. Aliniază pe centru acest câmp.
4. Pagina "Despre noi"
    1. Creează un fișier nou, denumit `despre-noi.html`.
    2. În acest fișier introdu același head, bootstrap-ul, aceeași bară de navigare și același footer ca și în fișierul `index.html`. Conținutul din mijloc va fi diferit.
    3.  Afișează un `h1` cu titlul acestei pagini.
    4. Recomand să ai tot conținutul îmbrăcat într-un `.container`, ca să nu se întindă pe toată lățimea paginii.
    5. Adaugă două paragrafe de text.
    6. Sub text introdu un Collapse (vezi exemple în documentația Bootstrap), cu un link pe care să fie scris "Citește mai mult". La expandare să se mai deschidă câteva paragrafe de text.
    7. Adaugă o secțiune nouă, la început de secțiune introdu titlul "Echipa".
    8. Folosește carduri de Bootstrap pentru a afișa fiecare membru de echipă (atenție, șterge din cod-ul cardului limitatorul de lățime `style="width: 18rem;"`).
    9. Fiecare card trebuie să fie într-o coloană. Trebuie să avem 3 coloane cu 3 membri de echipă.
    10. Adaugă o poză pătrată, un nume și o funcție a membrului de echipă.
5. Pagina "Contact"
    1. Creează un fișier `contact.html`, în care să faci același lucru ca și pe pagina "Despre noi".
    2. Adaugă la conținut orice dorești. Sugerez să încerci să faci **embed** la o hartă de Google Maps (Google It!).
6. În bara de navigare afișează 3 link-uri: Home, Despre noi și Contact. Fiecare să ducă spre fișierul corespunzător. Link-ul ar trebui să aibă cale relativă, adică să arate în acest fel: `<a href="despre-noi.html"...`. Actualizează bara de navigare în **fiecare** dintre clele 3 fișiere.

![index.html](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/18218380-fb5e-4ec7-80c0-aee14a1122cb/home.png)

index.html

![despre-noi.html](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/99be7d6f-7f5b-41d1-b4e1-35dc33b5525d/despre-noi.png)

despre-noi.html