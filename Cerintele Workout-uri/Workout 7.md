# 7. PHP

## Introducere

Sper că ai observat că în toate 3 fișiere (index.html, despre-noi.html și contact.html) există niște elemente care se repetă. În acestea se repetă head-ul, bara de navigare și subsolul (footer-ul). Partea din mijloc este diferită în funcție de fiecare pagină.

Dacă, acum voi cere să introduci un link nou în bara de navigare, să înlocuiești iconița sau să modifici textul din footer, va trebui să faci aceste modificări în **fiecare fișier HTML**! În acest moment avem doar 3 fișiere însă, în proiecte mai mari, numărul de fișiere este mult mai mare. Modificarea elementelor repetitive în fiecare fișier este o muncă de rutină, plictisitoare.

Pentru a evita munca repetitivă, ar fi frumos să externalizăm zonele care se repetă, să le mutăm într-un fișier extern și să apelăm această secvență de cod în fiecare dintre pagini. În aceast caz modificările ulterioare se vor face doar în fișierul externalizat iar modificarea va fi vizibilă în fiecare dintre paginile în care este apelat acel fișier.

## Sarcini

1. Externalizarea fragmentelor de cod repetitive:
    1. Creează un folder cu numele "includes" în care vei depozita diferite bucăți de cod ce vor fi incluse în pagini.
    2. În folderul "includes" creează un fișier `header.php` și un fișier `footer.php`. Populează aceste fișiere cu acel conținut din site care se repetă pe toate paginile în partea de sus a site-ului și, respectiv, în partea de jos.  De exemplu, fișierul `header.php` ar trebui să conțină atât tag-urile `<html>`, `<head>` cu întregul său conținut și `<body>`. Tag-ul de închidere `</body></html>` ar trebui să fie în fișierul `footer.php`, la fel și textul de copyright.
    3. În toate paginile (index.php, despre-noi.php și contact.php) înlocuitește acel conținut repetitiv cu fișierele `header.php` și `footer.php`, incluzându-le folosind funcția cea mai potrivită după părerea ta.
2. În footer,  în drept cu textul de copyright, afișează anul curent, cu ajutorul funcției PHP. 
3. Pentru numerele afișate pe home page, cele cu numărul de participanți la modul, aplică o funcție de PHP care să stilizeze (formateze) numărul în așa fel, ca să se aplice separator de mii. De exemplu, numărul "23456" să se afișeze "23.456".
4. Folosind structura de control `if - else`, verifică dacă numărul total de participanți (rezultat după sumarea participanților de la toate modulele) este sau nu mai mare decât 50000. Dacă este mai mare sau egal, acesta să fie afișat în tag-ul `<strong></strong>`. 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/785eb18a-322a-446c-8e30-7f57f594455b/home-tema-7.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/785eb18a-322a-446c-8e30-7f57f594455b/home-tema-7.png)