1. Time to start coding your first real PHP webpage! You're going to start with one of the classics, saying "Hello!" to your user and, by the end of these cards, you'll be making a number guessing game for the user to play!

2. So, to begin with, every PHP webpage will have at least a little bit of HTML in it. Start by making a really basic one by typing this code into your **index.php** and saving it.

   ```php
    <!DOCTYPE html>
    <html>
    <head>
    <title>My PHP webpage</title>
    </head>

    <body>
    This is just HTML text, it is not clever like your PHP text will be!
    </body>

    </html>
   ```

   The things in the angle brackets \(`< >`\) are called **HTML tags** and you'll be coming across a few of them in these cards. There are lots more, though, and you can learn about them in the HTML Sushi Cards and in loads of other places online!

3. Run that page and you'll see a basic HTML page. To begin with, your PHP page is going to look pretty similar, but very quickly you'll be using the power of PHP to do things that HTML never could alone! To get started, replace that HTML text with some special PHP code.

   ```php
    <body>
        <?php
            echo "Hello everyone! This is my first PHP program!";
        ?>
    </body>
   ```

   Notice that PHP code always appears inside `<?php` and `?>`. This is so the computer can tell which parts are PHP and which parts are HTML. Using these, you can put PHP code anywhere inside the HTML.  
    Also, notice that the PHP code always ends each line with a semicolon \(`;`\). This is so PHP knows to end this command and start another. If you forget to do this, PHP can get very confused.

4. Now save and run your PHP file. Congratulations! If it all worked, you've just written your first PHP webpage!



