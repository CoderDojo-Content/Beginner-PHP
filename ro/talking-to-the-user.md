1. Bine, deci acum poți lua informația dintr-o variabilă și o poți arăta utilizatorului cu `echo`, dar cum poți lua răspunsul de la utilizator? Până la urmă acesta e un joc de ghicit, deci ai nevoie de o modalitate să colectezi încercările lor!

2. Vei avea nevoie de o combinație de HTML și PHP pentru asta. Codul HTML va fi nou, chiar dacă ai citit Cărțile Sushi HTML. Programul tău PHP va folosi multe **formulare**, le poți vedea pe aproape orice website și sunt simplu de implementat!

   ```php
   <form method="get">
   Răspunsul tău: <input type="text" name="guess"/>
   </form>
   ```

   Un formular HTML e o idee simplă: elemente—precum casete de text, meniuri drop-down, casete de bifat sau butoane—sunt folosite pentru a colecta informații de la utilizatori și pentru a le trimite către programul tău PHP. Uneori, răspunsurile sunt trimise către utilizatori. Vei trimite astfel de răspunsuri în jocul tău.

3. E timpul să adaugi un formular pe pagina ta! Vei folosi variabile PHP și linii `echo` pentru a crea formularul în loc să folosești doar HTML. Ce trebuie să faci e să adaugi următoarele linii sub cele 2 linii `echo` deja existente:

   ```php
   echo "<form method="get">";
   echo "Răspunsul tău: <input type="text" name="guess"/>";
   echo "</form>";
   ```

   Run this code and see what happens!

4. Well, that didn't quite work right, did it? Any idea why? It's because of the double quotes in `<form method="get">`. PHP isn't smart enough to recognise that they are part of the HTML tag; it reads them as the end of the **string** of text that `echo` is trying to insert into the page. After that, it's looking for a semicolon \(`;`\) but instead it finds `g` and gets very confused! This kind of problem can come up quite often either because you've forgotten which kind of quotes to use or you're copying from another of your programs and used quotes differently there. Luckily, it's very easy to fix. Just put a backslash \(`\`\) in front of your all your double quotes \(don't forget the ones in the **input **tag!\) like this, to **escape** the normal rule of ending the **string**!

   ```php
   echo "<form method=\"get\">";
   ```

5. Run the code again! Now you've got somewhere for your user to put their text! Type something in and press the enter key. Watch the page URL in the browser and notice what changes!



