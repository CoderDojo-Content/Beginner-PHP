1. C’est l’heure de coder votre première page en PHP! Vous allez commencer par un grand classique, dire bonjour à vos utilisateurs, mais d’ici la fin de ce tutoriel vous saurez créer un petit jeu où vos utilisateurs devront deviner des nombres!

2. Toute page codée en PHP doit contenir au moins un peu de HTML. Pour l’instant, intégrez ce code de base dans votre **index.php** et enregistrez la page.

   > `<!DOCTYPE html>`
   >
   > `<html>`
   >
   > `<head>`
   >
   > `<title>Ma page PHP</title>`
   >
   > `</head>`
   >
   >
   >
   > `<body>`
   >
   > `Ceci est juste du texte HTML, il n’est pas aussi malin que celui que vous écrirez en PHP !`
   >
   > `</body>`
   >
   >
   >
   > `</html>`



   Le contenu entre crochets \(&lt;&gt;\)sont des **balises HTML** et vous en trouverez en grand nombre à travers ce tutoriel. Il y en a beaucoup d’autres, vous pouvez en apprendre plus à leur sujet dans les Cartes Sushi HTML et à bien d’autres endroits sur Internet!



   3/ Lancez cette page et vous verrez une page HTML basique. Au début, votre page PHP va ressembler fort à celle-ci, mais très rapidement vous apprendrez à utiliser le pouvoir de PHP pour faire des choses que le HTML ne saurait jamais faire!

   Commençons à remplacer ce texte en HTML par du code PHP.

   ```
   <
   body
   >
   ```

   ```
   <
   ?php
   ```

   ```
   echo
   "
   Bonjour tout le monde ! Voici mon premier programme en PHP!
   "
   ;
   ```

   ```
   ?
   >
   ```

   ```
   <
   /body
   >
   ```

   Notez bien que le code PHP apparaît toujours entre les balises&lt;?phpet?&gt;. Ceci afin que l’ordinateur puisse identifier quelles parties du code sont en PHP et lesquelles sont en HTML. En les utilisant, vous pouvez insérer du code PHP n’importe où dans le HTML.

   Notez également que le code PHP termine chaque ligne par un point-virgule \(;\). Cela permet à PHP de comprendre que la commande est terminée et qu’il peut passer à la suivante. Si vous oubliez de terminer vos lignes par un;vous allez avoir quelques surprises.



   4/ Enregistrez et lancez votre fichier en PHP.

   Félicitations! Si tout a bien fonctionné, vous venez d’écrire votre première page en PHP!

  




    n����5



