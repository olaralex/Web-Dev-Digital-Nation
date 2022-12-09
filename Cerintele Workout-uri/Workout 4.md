# 4. Bootstrap

1. Include Bootstrap.
    1. Accesează site-ul oficial Bootstrap, ultima versiune, și găsește pagina cu instrucțiunile de utilizare.
    2. Copiază și include fișierele `.css` și `.js` în fișierul tău `.html` 
2. Zona de prezentare generală (cea cu textul pe centru) o vom reface, folosindu-ne de clasele Bootstrap.
    1. Șterge css-ul care definește lățime maximă de `600px`și cel care poziționează pe centru acest conținut. Nu vom mai avea nevoie de ele deoarece vom folosi Bootstrap. 
    2. Adaugă elementului părinte (pentru această secțiune) clasa `container` pentru ca acest element să aibă o lățime maximă și să fie poziționat pe centru. 
    3. Dacă ai făcut totul corect, vei observa că conținutul are o lățime mai mare decât avem nevoie (în screenshot-urile anterioare e maximum 600px, aproximativ). Din acest motiv vom mai adăuga niște elemente care să limiteze lățimea conținutului. În interiorul elementului cu clasa `container` adaugă element cu clasa `row` în care vom adăuga un element cu clasa specifică coloanei. În scopuri didactice nu voi preciza exact ce clasă să folosești, doar voi descrie rezultatul pe care îmi doresc să îl obții și mă aștept să identifici tu clasa.
    4. Pe dispozitivele cu ecrane mici conținutul va ocupa tot spațiul disponibil pe lățime (întreg container).
    5. Pe ecranele de la `md` și până la `lg` lățimea conținutului să fie de 10 coloane. 
    6. Pe ecranele `lg` și mai mari lățimea conținutului să fie de 6 coloane. 
    7. Ar fi nevoie ca conținutul să fie poziționat pe centru, din acest motiv vom atribui elementului părinte (cel cu clasa `row`) încă o clasă de Bootstrap, care de fapt face acleași lucru ca și Flexbox: aliniază elementele copii pe mijloc. Identifică tu în documentația Bootstrap sau în Google cum se numește această clasă și aplic-o.
3. Zona de caracteristici.
    1. Păstrează un div ca element părinte, pentru care vei defini culoarea de fundal să fie gri. 
    2. Adaugă padding de sus și de jos, în așa fel ca să nu fie elementele interioare lipite de marginea fundalului gri (folosește clasa `py-5` care înseamnă padding pe axa y, adică cea verticală).
    3. Adaugă în interior un `container`, pentru ca conținutul să nu mai depășească lățimea maximă a acestui container.
    4. În interiorul containerului adaugă un element cu clasa `row`, acesta va fi părintele pentru cele 3 coloane (atenție, nu adăuga clasa `container` și `row` la același eleemnt).
    5. Șterge din fișierul CSS tot ce ai scris în Media Query legat de pozițio
    6. Fiecărei coloane adaugă-i clase de Bootstrap, în așa fel ca acestea să se alinieze una lângă cealaltă pe ecranele mari, de la braekpoint-ul `md` și în sus, adică să ocupe o treime din ecran ceea ce în Bootstrap reprezintă 4 coloane din 12.
    7. Pentru breakpoint-ul `sm` afișează prima coloană pe toată lățimea ecranului, iar coloanele 2 și 3 să fie una lângă cealaltă și să ocupe jumătate din lățimea 
    8. Pentru ecranele mai mici de breakpoint-ul `sm` afișează toate coloanele una sub cealaltă, pe toată lățimea ce ecran. 
    *ATENȚIE: Punctele 6, 7 și 8 se implementează doar prin intermediul claselor adăugate în codul HTML și fără vreo linie de cod CSS. Toate clasele, modul de utilizare și descrierea lor sunt în documentația oficială Bootstrap. NU voi detalia ce clase anume să folosești pentru a te provoca să cauți și să încerci.*