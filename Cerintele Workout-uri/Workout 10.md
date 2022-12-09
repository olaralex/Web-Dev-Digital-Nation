# 10. WordPress

1. Tema child
    1. Creează o temă child pentru tema părinte "Understrap".
    2. Creează în folderul temei child fișierul `functions.php` și adaugă în el conținutul care permite conectarea fișierelor de stiluri din tema părinte și copil:
        
        ```php
        <?php 
            add_action( 'wp_enqueue_scripts', 'wp_understrap_child_enqueue_styles' );
            function wp_understrap_child_enqueue_styles() {
                $parenthandle = 'understrap-style';
                wp_enqueue_style(
                    'child-theme-styles', 
                    get_stylesheet_uri(), 
                    array(),
                    filemtime(get_stylesheet_directory().'/style.css')
                );
            } 
        ```
        
    3. Activează tema child din panoul de administrare.
    4. În cazul în care s-au pierdut unele stilizări, accesează secțiunea *Appearance → Customize* și setează din nou stilizările necesare.
2. Home Page
    1. Creează în tema child un folder `page-templates`.
    2. În interiorul acestuia creează un fișier cu numele `template-home.php`.
    3. Pentru ca acest fișier să fie vizibil din panoul de administrare, la început de fișier, după ce deschizi tag-ul de PHP, adaugă un comentariu cu `Template Name: Home page`.
    4. În interiorul fișierului vom adăuga codul specific unui loop standard de WordPress, dar în același timp vom păstra structura cu clasele și ID-urile din tema părinte. Pentru a vedea structura fișierelor gândită de autorul temei, vom accesa din tema părinte fișierului `page.php` și putem să copiem de acolo întregul conținut în noul nostru fișier, curățându-l de ceea ce nu avem nevoie.
    5. Vom avea nevoie de o pagină practic goală, care nu afișează alte texte. În aceasta vom introduce propriul nostru conținut personalizat (codul pe care l-am scris noi personal), așa că în urma eliminării codului de care nu avem nevoie, vom obține următoarea structură:
        
        ```php
        <?php
        /**
        * Template Name: Home Page
        */
        
        // Exit if accessed directly.
        defined( 'ABSPATH' ) || exit;
        
        get_header(); ?>
        
        <div class="wrapper" id="page-wrapper">
        
        	<div id="content" tabindex="-1">
        
                <main class="site-main" id="main">
        
                    <?php
                    while ( have_posts() ) {
                        the_post(); ?>
        
                        AICI VINE CONȚINUTUL PAGINII
        
                    <?php } ?>
        
                </main><!-- #main -->
        
        	</div><!-- #content -->
        
        </div><!-- #page-wrapper -->
        
        <?php
        get_footer();
        ```
        
3. Vrem ca pe home page să afișăm conținutul pe care l-am dezvoltat în proiectul anterior (HTML/PHP)
    1. Deschide fișierul `index.php` din tema veche (cea din folderul demo).
    2. Copiază tot conținutul cu excepția fragmentelor în care includem header și footer. Avem nevoie doar de conținutul propriuzis. 
    3. Introdu acel conținut în fișierul template-ului la care lucrăm. 
    4. Copiază stilurile CSS care sunt legate de această pagină, din fișierul `style.css` din folderul demo, în fișierul `style.css` din tema child a site-ului Wordpress.
    5. Deschide site-ul pe prima pagină și verifică dacă ți se afișează conținutul proaspăt migrat.
4. Renunță la padding-urile date de DIV-ul cu clasa `.wrapper`.
Probabil ai observat că există un spațiu între bara de navigare și slider. Ar fi mai frumos dacă aceste elemente vor fi lipite între ele. Pentru asta va trebui să suprascriem codul CSS al site-ului, și vom aplica propriul nostru CSS care să se propage doar pentru Page Template-ul folosit de noi în această pagină, nu și pentru alte pagini din website.
    1. Inspectează pagina din browser și găsește ce clase sunt aplicate pe tag-ul `body`.
    2. Alege clasa care face referință la page template-ul nostru și folosește-te de ea, pentru a defini o regulă CSS.
    3. În fișierul `style.css` din tema child adaugă această regulă CSS, aplicând stilurile de `padding: 0`.
    4. În urma acestor modificări ar trebui să vezi pe home page, lipite, bara de sus (cea cu meniul) și slider-ul. Între ele nu ar trebui să fie niciun spațiu gol.
5. Facem butoanele de pe Home Page să fie funcționale:
    1. Butonul secundar "Cere detalii" ar trebui să fie link spre pagina de contact. De exemplu: `<a href="/contact/" class="btn ...`
    2. Butonul primar, la click, ar trebui să deschidă un element *Modal.* 
    *Notă: În partea de conținut momentan nu afișăm nimic. Ulterior vom avea un formular de contact cu următoarele câmpuri: Nume, Email, Telefon și butonul "Înscrie-mă".*
    3. Codul pentru funcționalitatea de Modal îl găsești în documentația Bootstrap v5.1.3.
    4. Afișează elementul Modal alineat vertical pe centru și de mărimea *small* (în documentație este explicat cum se procedează).
    5. Titlul de sus înlocuiește-l cu un text relevant iar butoanele de jos, din zona `modal-footer` trebuiesc șterse.