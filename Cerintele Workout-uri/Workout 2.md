# 2. HTML & CSS

## Sarcina

Reprodu pagina HTML din screenshot-ul atașat. Îți voi pune la dispoziie explicații cu structura paginii pentru a-ți ușura munca.

## Mod de lucru

- Creează un fișier HTML și unul CSS.
- Include fișierul CSS în cel HTML.
- Deschide fișierul HTML în browser și urmărește periodic ce se afișează, după fiecare fragment de cod adăugat.
- Poți utiliza alte culori pentru header, fundal, text.
- Poți utiliza alte imagini și alte texte. **Important** este să păstrezi același număr de elemente, aceeași poziționare și structură.

## Structura

- Bară de navigare pe care a fost aplicată o culoare de fundal.
    - În interiorul barei de navigare avem un meniu. Acest meniu reprezintă o listă neordonată, adică este format din părintele `ul` cu fiecare elemnt `li` în interiorul căruia avem câte un link. Link-ul ar trebui să aibă `padding` ca să nu fie lipit textul de margini. Link-urile, momentan, nu au nicio destinație către care să ducă.
- Zona de prezentare generală. Aceasta nu are culoare de fundal, în schimb are conținutul alineat pe centru, niște spațiere `padding` de sus și de jos a câte `50px`. Acest element are o lățime maximă de `600px`. Putem observa acest lucru din textul mic care trece din rând nou după cuvântul "megna" și după cuvântul "convallis". Dacă nu aș fi definit această lățime maximă, acel text s-ar fi extins pe toată lățimea paginii.
    - Primul element din interior este un antent principal `h1`.
    - Urmează un antet mai puțin important, `h2`.
    - Apoi avem un paragraf de text. În HTML paragraful are eticheta `p`.
    - Două butoane (care momentan nu au niciun efect).
- Zona cu caracteristici. Această zonă are o culoare de fundal și `padding` de sus și de jos, la fel ca elementul de mai sus.
    - În interior avem 3 elemente identice ca structură însă diferite ca conținut. Aceste elemente ar trebui să aibă eticheta `div`, însă acesta inițial este de tip `block`. În CSS ar trebui să îi definești tipul `inline-block`, pentru ca ele să se poată alinia într-o linie. Apoi să definești pentru acestea o lățime de cel mult 1/3 din pagină, pentru ca ele să încapă unul lângă celălalt. Fiecare element are în interior:
        - Imagine reprezentativă. Această imagine trebuiește făcută cerc cu ajutorul CSS (implicit ea este pătrată). Imaginea mai primește și un `border` de `5px` grosime și de culoare gri. Poți folosi aceeași imagine sau imagini diferite pentru fiecare dintre acele 3 elemente.
        - Antent `h4`.
        - Paragraf cu descriere.
- Footer (subsol). Acesta are și el aceeași spațiere ca și cele anterioare. Conținutul este alineat pe centru. Conținutul este:
    - Imagine care are rol de Logo. În screenshot am folosit drapelul României. Poți folosi orice imagine însă să îi definești lățimea maximă de `100px`.
    - Un formular `form` cu `label` care este textul din față, un `input` de tip email și un buton de tip `submit`. Momental nu contează partea funcțională a formularului. Contează doar să îi construim structura.
    - Un simplu text de copyright.
    

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2ae9f7d1-f52e-4bcc-9efa-db785034782b/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2ae9f7d1-f52e-4bcc-9efa-db785034782b/Untitled.png)