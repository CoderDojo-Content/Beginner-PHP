1. The text that appeared on the end of the URL is called a *query parameter* and you can have loads of them on the same URL. The form automatically added one (because you set `method='get'`), but you could just as easily type them in, separated by semicolons. PHP reads the end of the URL for the page it's loaded on and turns all the query parameters into something called a *key, value array*. You don't need to know exactly what that is right now, we'll go into it in a later Sushi Card series. What you do need to know is how to get values out of it.
2. All you need to do to get a value out of the array is pass in the key of a value that's in there. Since your form adds the `guess` field, that's the one you'll be looking for. You'll want to *assign* that value to a *playerGuess* variable, so add this line just before all your `echo` lines:
    ```php
    $playerGuess = $_GET['guess'];
    ```
3. Now, remind the player what their last guess was by adding another `echo` just before the input form:
    ```php
    echo "Your last guess was {$playerGuess}.<br />";
    ```
    Run the code. Now you're taking input from your player and giving it back to them. Very cool!

4. Try removing all the query parameters from the URL and reloading the page. Notice that you now get "Your last guess was ."  
That's not ideal. What you want to happen is:
    * **if** there's a value yet (maybe they haven't made a guess yet)
        * if so, show the message about the last guess

5. PHP can figure all this out and do it for you! You just need to use an `if` statement.  
An `if` statement uses a test (in brackets), that has an answer that's either *true* or *false* and, if it's true, a piece of code to run. You can do this to check if your variable contains anything like this:
    ```php
    if(!empty($playerGuess)){
        echo "Your last guess was {$playerGuess}.";
    } 
    ```
    Here `empty()` is a special piece of PHP that checks whether the variable inside its brackets has a value and answers either *true* if it doesn't or *false* if it does. The `!` before it reverses this answer, turning a *true* into a *false* and a *false* into a *true*.  
    Replace `echo "Your last guess was {$playerGuess}.";` with the code above and test it with and without answers to see it working.