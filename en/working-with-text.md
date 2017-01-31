1. Now it's time to start working on your game! The first thing you're going to need is to teach the player the rules.  
   You might want to change things like the smallest and biggest numbers, or the number of guesses you're going to give the player. If you wrote out the rules with plain HTML, you'd have to go back and re-write them every time you changed any of those things. You don't need to do that, though. You can use PHP and **variables** to include the numbers as part of your text!

2. First, you're going to need to to update your text, so change the PHP code on your page to this:

   ```php
   echo "I've picked a number between 1 and 9<br />";
   echo "You will have 5 chances to try to guess my number!";
   ```

   The `<br />` is a piece of HTML that tells the browser to start a new line after it. You can put any HTML inside your PHP and it will be treated exactly as if it had been written as HTML.

   Notice that you're using double quotes \(`"`\) around your text instead of single quotes \(`'`\), for two reasons:

   * PHP will get confused if you use an apostrophe inside of single quotes. Try it and see! What happens, and why?
   * PHP will do something special inside of double quotes that it won't inside of single quotes, which you'll see below.

3. Now it's time for you to start adding **variables**! These are labels that you can use to store values, like a **string** of text or a number. PHP remembers those values and lets you use the values later by using their label. This lets you set a value once and use it loads of times in your program. If you were building a website like Facebook, you would use a **variable** for the user's name and just us that label everywhere you wanted it.  
   In PHP, all variable names start with a dollar sign \(`$`\) and are usually written in **camelCase**, where the first word starts with a small \(lowercase\) letter, there are no spaces, and any later words start with capital \(uppercase\) letter.

   So, time to add your first **variables**! Put this line in, inside the `<?php` but before the `echo` lines

   ```php
   $minValue = 1;
   $maxValue = 9;
   $guesses = 5;
   ```

   All of these **variables** are numbers, but you'll be working with text variables later.

4. Now, update your two `echo` lines so they look like this:

   ```php
   echo "I've picked a number between {$minValue} and {$maxValue}<br />";
   echo "You will have {$guesses} chances to try to guess my number!";
   ```

   Notice the curly braces \(`{` and `}`\) around the variable names to tell PHP not to treat them like regular text!

5. Run your program and see what happens. Then try changing the values of some of the variables and run it again. Just make sure to set everything back to the way we've left it here before moving on!



