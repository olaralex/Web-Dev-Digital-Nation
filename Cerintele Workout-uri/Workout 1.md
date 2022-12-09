# 1. Noțiuni introductive

1. Instalează Visual Studio Code.
    1. Din coloana laterală din stânga accesează **Extensions**, găsește extensia cu numele "PHP Intelephense", apasă pe iconița se detări din dreapta, selectează **Extension Settings**. În pagina de setări derulează pagina până jos, la secțiunea "Intelephense: Stubs", apasă butonul **Add Item** și selectează **wordpress**. Asigură-te că ai adăugat Wordpress în listă, astfel vei evita niște erori în viitor.
    2. Instalează niște extensii suplimentare pentru VSCode: PHP Extension Pack, HTML CSS Support și altele la alegere.
2. Instalează Local by Flywheel și creează un proiect de **WordPress** cu numele de forma: **`nume-prenume`**, unde să introduci fără diacritice și fără spații, doar cu cratime, numele tău complet.
3. După crearea proiectului și pornirea acestuia te asiguri că WordPress funcționează... și îl ignori. La această etapă folosim serverul local pentru a lucra cu PHP și nu avem nevoie de WordPress.
4. În interfața Local, sub numele proiectului este un text gri cu adresa în care se află fișierele proiectului. Apasă pe săgeata din dreptul adresei sau găsește manual adresa fișierelor. Deschide folderul **app** și vei găsi folderul **public** în care se află site-ul propriuzis. Trage în Visual Studio Code (VSC) acest folder sau din VSC alege să deschizi un proiect și găsește acest folder. 
5. În interfața VSC, în folderul în care se află **wp-content, wp-admin** etc., creează un nou folder numit **demo**. În el vom lucra.
6. În folderul **demo** creează fișierul index.html în care să introduci structura de bază a paginii HMTL (Google It) și afișează textul "Hello World!". Deschide în browser și testează fișierul.
7. Creează un fișier styles.css pe care să îl incluzi în fișierul index.html și în care să elimini marginile default pentru body, definite de browser.