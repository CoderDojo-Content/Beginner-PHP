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

   Rulează acest cod și vezi ce se întâmplă!

4. Păi se pare că n-a mers, așa-i? Ai idee de ce? E din cauza ghilimelelor duble în`<form method="get">`. PHP nu știe să recunoască faptul că sunt parte dintr-un tag HTML; le interpretează ca fiind finalul **șirului de caractere** pe care `echo` încearcă să-l introducă în pagină. Apoi, caută un punct și o virgulă \(`;`\), dar în locul său găsește litera `g` și se bulversează. Astfel de probleme pot apărea deseori fie când uiți ce fel de ghilimele să folosești, fie când copiezi o porțiune dintr-un alt program de-al tău unde ai folosit ghilimelele puțin diferit. Din fericire e simplu să repari problema printr-un backslash \(`\`\) adăugat în fața ghilimelelor duble \(nu le uita pe cele din tag-ul **input**!\), pentru a **anula** regula obișnuită de a sfârși un **șir de caractere**.

   ```php
   echo "<form method=\"get\">";
   ```

5. Run the code again! Now you've got somewhere for your user to put their text! Type something in and press the enter key. Watch the page URL in the browser and notice what changes!



