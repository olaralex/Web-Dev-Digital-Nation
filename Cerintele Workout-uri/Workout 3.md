# 3. HTML & CSS

1. Aplicând pe tag-ul `ul` din bara de navigare `display: flex`, afișează elementele din meniu orizontal, unul lângă celălalt. 
2. Ascunde sublinierea de pe link-urile din meniu. Iar atunci când vizitatorul trece cu mouse-ul peste un oarecare link, aplică-i acestuia o culoare de fundal semitransparentă, cu ajutorul pseudoselectorului `:hover`.
3. În bara de navigare, în partea dreaptă, în drept cu meniul, afișează o iconiță de telefon care să reprezinte un link. Iconița de telefon de preferat să fie *unicode symbol*, nu imagine. Pentru a o poziționa pe dreapta va fi nevoie de `display: flex` pentru elementul părinte și mai e nevoie de indicat ca elementele copii să fie alineate în capete diferite. 
*Notă: poți folosi orice altă iconiță de telefon pe care o găsești pe internet. Ea nu trebuie să coincidă cu cea din exemplul atașat.*
4. Cu ajutorul `font-size` fă iconița telefonului mai mare decât celălalt text, de exemplu să reprezinte `1.5rem` ceea ce înseamnă că trebuie să aibă mărimea 1.5 față de mărimea font-ului de bază.
5. Aliniază pe axa Y (verticală) meniul din stânga și telefonul din dreapta în așa fel ca să fie centrate, adică să nu rămână sub meniu mai mult spațiu decât deasupra. Acest rezultat poate fi obținut cu ajutorul proprietății `align-items` aplicată pe elementul părinte.
6. În secțiunea de caracteristici, cele afișate în 3 coloane, renunță la `display: inline-block` sau la alte metode prin care ai obținut afișarea în 3 coloane și folosește `display: flex`. 
7. Adaugă în CSS un media query, pentru ca pe ecranele cu lățimea mai mică de `900px` primul element din lista cu caracteristici să rămână în primul rând iar următoarele două elemente să fie în al doilea rând, unul lângă celălalt, în două coloane. 
*Notă: În screenshot este reprezentată varianta de afișare pentru ecrane cu lățime mai mică de 900px. Pe ecranele cu lățime mai mare toate 3 elemente ar trebui să se afișeze într-un singur rând.* 
8. Opțional, poți adăuga secțiuni și elemente în plus, pentru a exersa Flexbox și Media Queries, deoarece sunt niște concepte foarte des utilizate și dezvoltarea unui automatism în acțiuni este foarte utilă.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a5fe1808-246b-4c49-a825-e22371e4fd0f/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a5fe1808-246b-4c49-a825-e22371e4fd0f/Untitled.png)