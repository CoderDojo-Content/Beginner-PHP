1. Acum e timpul să începi lucrul la jocul tău! Primul lucru pe care trebuie să-l faci e să înveți utilizatorul care sunt regulile de joc. E posibil să vrei să schimbi anumite detalii, precum cel mai mic sau cel mai mare număr, sau numărul de încercări pe care le are utilizatorul. Dacă ai scrie regulile doar în HTML, va trebui să le rescrii de fiecare data când vei dori să le modifici. Nu trebuie să faci asta însă. Poți folosi PHP și **variabile** pentru a include numerele în text!

2. Mai întâi, va trebui să înlocuiești codul PHP de pe pagina ta cu cel de mai jos:

   ```php
   echo "Am ales un număr între 1 și 9<br />";
   echo "Vei avea 5 încercări să ghicești numărul meu!";
   ```

   `<br />` e bucata de HTML care îi spune browser-ului să înceapă o linie nouă. Poți pune orice cod HTML în interiorul codului PHP și va fi procesat de parcă ar fi fost scris ca HTML.

   Poți observa că folosești ghilimele duble \(`"`\) în jurul textului tău în loc de ghilimele simple \(`'`\), din două motive:

   * PHP nu va ști ce să facă dacă folosești un apostrof între ghilimele simple. Încearcă și vezi! Ce se întâmplă și de ce?
   * PHP va face ceva special între ghilimele duble, dar nu între ghilimele simple, ceea ce vei vedea puțin mai jos.

3. E timpul să adaugi **variabile**! Acestea sunt etichete pe care le poți folosi să păstrezi valori precum un **șir de caractere** sau un număr. PHP ține minte aceste valori și te lasă să le folosești mai târziu doar folosing etichetele. Acest lucru te ajută să setezi valoarea o singură data și să o folosești de mai multe ori în programul tău.  
   În PHP, toate variabilele încep cu semnul dolarului \(`$`\) și sunt de regulă scrise în **camelCase**, unde primul cuvânt începe cu literă mică, nu există spații, și orice cuvânt care urmează începe cu literă mare.

   Adaugă aceste variabile după `<?php`, dar înainte de liniile `echo`:

   ```php
   $valoareMin = 1;
   $valoareMax = 9;
   $incercari = 5;
   ```

   All of these **variables** are numbers, but you'll be working with text variables later.

4. Now, update your two `echo` lines so they look like this:

   ```php
   echo "I've picked a number between {$minValue} and {$maxValue}<br />";
   echo "You will have {$guesses} chances to try to guess my number!";
   ```

   Notice the curly braces \(`{` and `}`\) around the variable names to tell PHP not to treat them like regular text!

5. Run your program and see what happens. Then try changing the values of some of the variables and run it again. Just make sure to set everything back to the way you've got it here before moving on!



