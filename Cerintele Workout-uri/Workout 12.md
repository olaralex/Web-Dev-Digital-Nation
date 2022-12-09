# 12. WordPress

1. Din panoul de administrare *Appearance → Customize → Site Identity* setează o imagine Logo. Dacă imaginea este prea mare, din CSS limitează-i înălțimea.
2. Personalizăm widget-ul din Footer accesând din panoul de administrare *Appearance → Widgets → Footer Full* și adăugând câteva widget-uri. Fiecare widget automat va ocupa câte o coloană în site.
    1. În primul element (widget) adaugă imaginea cu logo-ul (sau orice altă imagine).
    2. În al doilea, folosindu-te de Widget-ul *Paragraph* adaugă o descriere scurtă iar mai jos, folosind widget-ul *Custom HTML* adaugă un link care să arate a buton (folosind clasele Bootstrap) la click pe care să ajungem pe pagina *Despre Noi*.
    3. Pentru ca paragraful de text și butonul să rămână în aceeași coloană, folosește unul dintre widget-uri cu numele *Group* sau *Widget Group* și grupează mai multe elemente.
    4. Dacă nu mai înțelegi nimic din interfața din panoul de administrare, activează harta elementelor, denumită *List view*, din partea stângă-sus, buton de lângă titlul secțiunii *Widgets*, pe care este reprezentată iconița a 3 linii orizontale decalate.
    5. Pentru a treia coloană va trebui să creăm un meniu. Mergem în zona de meniuri, creăm un meniu și îl populăm cu *Custom Links* în care să avem link-uri spre Termeni și condiții, Politica de confidențialitate, Cookies dar și pagina Contact. Ne întoarcem în zona de adăugare Widget-uri, afișăm widget-ul *Navigation Menu* și selectăm meniul nou creat.
    6. În ultima coloană vom adăuga un Formular de abonare la newsletter. Din pagina de administrare a plugin-ului *Contact Form 7* creează un nou formular care să aibă doar câmpul *Email* și butonul *Înscrie-mă*. Copiază shortcode-ul formularului nou creat și afișează-l în coloana a 4-a folosindu-te de widget-ul *Shortcode*. Înainte de shortcode mai scrie un text introductiv, pentru a adăuga volum acestei coloane.
3. Secțiunea de Copyright.
Vom personaliza această secțiune, pentru asta va fi nevoie să facem o copie a fișierului care răspunde de afișarea acestei secțiuni. Copia fișierului se face din tema părinte în child theme.
    1. Copiază din tema părinte în child fișierul `footer.php` .
    2. Aplică pe secțunea de copyright niște clase de bootstrap, în așa fel încât fundalul să fie de culoarea dark, iar textul să devină alb.