# 11. WordPress

1. În panoul de administrare WordPress, din pagina de setări a plugin-ului Contact Form 7, creează formular de contact (pentru Modal-ul din Home Page) cu următoarele câmpuri: Nume, Email, Telefon și butonul "Înscrie-mă".
2. Copiază shortcode-ul formularului generat de plugin. Introdu-l în zona de conținut a Modal-ului din Home Page. Pentru ca un shortcode să se execute, este nevoie să te folosești de funcția de WordPress: `do_shortcode()`
3. În acest moment unica metodă de a modifica conținutul paginii este editarea directă a fișierului, accesând codul acestuia. În cele ce urmează vom face un upgrade care ne va permite să modificăm unele câmpuri direct din panoul de administrare WordPress. Un moderator al site-ului, care nu are acces la codul fișierului, va putea să modifice unele texte și acestea se vor afișa modificate în pagină. Vom face următoarele modificări:
    1. Deschide pagina de modificare a Home Page-ului și modifică titlul paginii. Înlocuiește titlul actual cu acea frază pe care o ai afișată pe site în tag-ul H1. În cazul meu fraza este *"Arta de a căuta informații în Google!"*.
    2. În codul paginii (fișierul `template-home.php`), în interiorul tag-ului H1, șterge textul și înlocuiește-l cu funcția de WordPress care răspunde de afișarea titlului paginii. Funcția se numește `the_title()`.
    3. În pagina de modificare a Home Page-ului,  în zona de conținut, introdu subtitlul din codul paginii și descrierea de sub el (important să ai textul pe centru și tag-ul H2 pe subtitlu).
    4. În fișierul `template-home.php` șterge subtitlul și descrierea. Afișează în locul lor funcția de WordPress care răspunde de afișarea conținutului paginii.
    *Notă: Butoanele trebuie să rămână la locul lor.* 
4. Următoarele exerciții sunt menite să exersăm utilizarea și modificarea fișierului `functions.php`. Vom aplica câteva modificări, cele mai simple dar și cu cel mai evident efect:
    1. Dacă te duci în panoul de administrare *→ Appearance → Widgets*, poți adăuga pentru *Right Sidebar* niște elemente de widget, pe care le poți vedea pe lateral în secțiunea de blog (în caz că nu ai dezactivat din *Customize* sidebar-ul). Adaugă câmp de search. 
    Dacă mergem pe site și scriem în acel câmp un cuvânt cheie, la rezultatele căutării vom primi atât Posts (adică articole) cât și pagini. De exemplu, folosind cuvântul *post* poți vedea în rezultatele căutării articolul *Hello world!* și pagina *Sample Page*, adică cele implicite. Ar fi fost util să păstrăm search-ul doar pentru articole iar în rezultatele căutării să nu apară pagini. Adaugă următorul fragment de cod în fișierul `functions.php` pentru a limita rezultatele căutării doar pentru Posts:
        
        ```php
        function search_results_filter($query) {
            if ($query->is_search) {
                $query->set('post_type', 'post');
            }
            return $query;
        }
        add_filter('pre_get_posts','search_results_filter');
        ```
        
    2. Adaugă următorul cod în fișierul `functions.php` pentru a modifica footer-ul afișat în panoul de administrare. Acest cod este util, de exemplu, pentru a lăsa propria semnătură în panoul de administrare când realizezi și livrezi un site clientului.
        
        ```php
        function remove_footer_admin(){
        	echo 'Site realizat de <a href="http://www.YOUR-SITE.com" target="_blank">Nume Prenume</a>';
        }
        add_filter('admin_footer_text', 'remove_footer_admin');
        ```
        
        ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6126669b-428a-499a-9b39-257bc369d88d/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6126669b-428a-499a-9b39-257bc369d88d/Untitled.png)
        
    3. Utilizatorii se pot autentifica pe site folosind atât emailul cât și numele de utilizator. WordPress îți oferă posibilitatea să dezactivezi logarea utilizatorior folosind adresa de email (va rămâne valabilă doar autentificarea folosind numele de utiilizator). Poți să introduci textul de mai jos în fișierul `functions.php` și să testezi această funcționalitate.
        
        ```php
        remove_filter( 'authenticate', 'wp_authenticate_email_password', 20 );
        ```
        
    4. În panoul de administrare WordPress, pe meniul *Dashboard* este pagina introductivă care are la început o zonă întitulată *"Welcome to WordPress!"*. Avem posibilitatea să ascundem această zonă, ca să nu ne deranjeze de fiecare dată când ne autentificăm. O putem face folosind codul de mai jos:
        
        ```php
        remove_action('welcome_panel', 'wp_welcome_panel');
        ```
        
        ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a163a555-179a-42fd-b29c-fb37ebbb2e14/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a163a555-179a-42fd-b29c-fb37ebbb2e14/Untitled.png)