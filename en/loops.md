1. You'll notice that now the count of guesses does go down to 4, but it never goes any lower! Any idea why? It's because of the way PHP works: Every time the page loads, the program runs again from the start, with no memory of the last time it ran! That means it always resets the value of `guessesLeft` to 5 and then, if a guess was made, subtracts 1. So, what you need to do here is store that value somewhere and pass it into the program the next time it runs. Well, you already have something like that: the form on the web page! You can write the current value of `guessesLeft` into the form and read it back out from `$_GET` later. Start with the writing, by updating your form creation code to look like this:

   ```php
    echo "<form method='get'>";
    echo "Your guess: <input type='text' name='guess'/>";
    echo "<input type='hidden' name='guessesLeft' value='{$guessesLeft}'/>";
    echo "</form>";   
   ```

   The type of the field is "hidden", so it won't be visible, but will be sent in on the URL. The value is set to the current value of 'guessesLeft'.

2. Now you need to pick up the value you've saved and write it into guessesLeft. This gets a little complicated, since there won't always be a value in the URL \(the first time the game is run, for example\). So you need to replace the current line `$guessesLeft = $guesses` with this:

   ```php
    $guessesLeft = $_GET['guessesLeft'];
    if(!isset($guessesLeft)){
        $guessesLeft = $guesses;
    }
   ```

   This code tries to get the value from the URL and, if it doesn't find it, leaves `guessesLeft` empty, which causes the code in the `if` statement to run, filling it with the value of guesses. The reason we didn't use `empty` here is because empty will give a **false** if the value is 0, which is going to happen here, when the player runs out of guesses. Try running the program again and you'll see that it all works now!

3. You may have noticed one last problem: The game doesn't end when you run out of guesses! We'll look at how to fix that, and how to use a secret number that actually changes, on the next card!



