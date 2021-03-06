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

   Toate aceste **variabile** sunt numere, dar vei lucra cu variabile de text mai târziu.

4. Acum înlocuiește cele două linii `echo` cu cele de mai jos:

   ```php
   echo "Am ales un număr între {$valoareMin} și {$valoareMax}<br />";
   echo "Vei avea {$incercari} încercări să ghicești numărul meu!";
   ```

   Observă acoladele \(`{}`\) din jurul variabilelor prin care PHP știe să nu le proceseze ca simplu text!

5. Rulează programul tău și vezi ce se întâmplă. Apoi încearcă să schimbi valorile unor variable și rulează-l din nou. Ai grijă să schimbi totul așa cum era, înainte să mergi mai departe! 



