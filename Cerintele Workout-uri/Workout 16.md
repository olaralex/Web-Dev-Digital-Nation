# 16. JavaScript

1. Creează fișierul `main.js` în folderul `/assets/js/` din Child Theme (aceste foldere nu există așa că și ele trebuiesc create).
2. Include acest fișier în Child Theme prin intermediul funcției `wp_enqueue_script()` în fișierul `functions.php`. Folosește codul de mai jos. Introdu fragmentul de cod color (fără rândurile gri de până la ...) pe lângă codul deja existent în fișier. Codul gri este doar exemplu pentru a-ți arăta unde trebuie să vină codul de includere script.
    
    ```php
    <?php 
        add_action( 'wp_enqueue_scripts', 'wp_understrap_child_enqueue_styles' );
        function wp_understrap_child_enqueue_styles() {
            ...
            wp_enqueue_script(
                'child-theme-script-main', 
                get_stylesheet_directory_uri().'/assets/js/main.js', 
                array('jquery'),
                1.0,
    						true
            );
    ```
    
3. Închiderea Modal-ului după ce utilizatorul a completat formuarul de înscriere:
    1. Introdu în fișierul `main.js` următorul fragment de cod JavaScript, care are rolul de a se declanșa fix în momentul când formuarul de contact este completat și trimis de către vizitator.
        
        ```jsx
        document.addEventListener( 'wpcf7mailsent', function( event ) {
            // AICI VINE CODUL CARE TREBUIE SĂ SE DECLANȘEZE DUPĂ TRIMITERE FORMULAR
        }, false );
        ```
        
    2. În interiorul fragmentului de cod de mai sus introdu un cod care va ascunde Modal-ul de Bootstrap. *Găsește exemplu cu acest cod JavaScript în documentația Bootstrap*.