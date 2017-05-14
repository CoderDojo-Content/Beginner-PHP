1. E timpul să codezi prima ta pagină web în PHP! Vei începe cu ceva clasic, prin a spune “Salut!” utilizatorului tău și, după ce vei parcurge toate cărțile, vei avea un joc de ghicit numere cu care utilizatorul paginii tale se poate juca!

2. Orice pagină web PHP are măcar puțin HTML în ea. Poți începe prin a construi o pagină simplă, copiind codul de mai jos în **index.php** și salvând fișierul.

   ```php
    <!DOCTYPE html>
    <html>
    <head>
    <title>Pagina mea web PHP</title>
    </head>

    <body>
    Acesta e doar text HTML, nu e la fel de deștept precum va fi codul tău PHP!
    </body>

    </html>
   ```

   Elementele dintre paranteze \(`< >`\) se numesc **tag-uri HTML** și le vei mai întâlni de-a lungul cărților. Sunt mult mai multe, mai complicate, și poți afla despre ele citind Cărțile Sushi HTML sau diferite surse online.

3. Rulează pagina și vei vedea o pagină HTML simplă. Pentru început, pagina ta PHP va arăta asemănător, dar foarte rapid vei folosi puterea PHP pentru a face lucruri pe care HTML nu le-ar putea! Pentru a începe, înlocuiește textul HTML cu un cod PHP special.

   ```php
    <body>
        <?php
            echo "Salutare! Acesta e primul meu program PHP!";
        ?>
    </body>
   ```

   Poți observa că acest cod PHP apare mereu între `<?php `și `?>`. Poți folosi aceste delimitatoare pentru a pune cod PHP oriunde într-un cod HTML, astfel calculatorul poate ști care părți sunt PHP și care sunt HTML. 

   De asemena, poți observa că o linie PHP se sfârșește mereu cu punct şi virgulă \(`;`\). Astfel PHP știe să termine o comandă și să înceapă alta. Dacă uiți să adaugi punct și virgulă, PHP o să devină foarte confuz.

Now save and run your PHP file. Congratulations! If it all worked, you've just written your first PHP webpage!



