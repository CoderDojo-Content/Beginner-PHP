1. Ok, so you can get information from a variable and show it to the player with `echo`, but how do you get information from the player? After all, this is a guessing game, so you need some way to collect their guesses!

2. You're going to use a combination of HTML and PHP to do this. The HTML you'll be using is going to be new, even if you've already done the HTML Sushi Cards, since they don't use many **forms** and your PHP programs will probably use a lot of them. You can see them on almost every website you use the internet and the code for them is pretty easy!    
```php
<form method='get'>
    Your guess: <input type="text" name="guess"/>
</form>
```
  A HTML form is a simple idea: controls—like text boxes, drop-down menus, check boxes or buttons—are used to collect information from users and send that information to your PHP program. Sometimes, responses are sent to the users. You'll be sending responses in your games.
3. Now, time to add a form to your page! So you can use PHP variables and other code in creating your form, you're going to use `echo` statements to create it, instead of just typing the HTML into the file. So, add the following below your two existing `echo` statements:
```php
echo "<form method='get'>";
echo "Your guess: <input type="text" name="guess"/>";
echo "</form>";
```
Run this code and see what happens!
4. Well, that didn't quite work right, did it? Any idea why? It's because of the double quotes in `<input type="text"/>`. PHP isn't smart enough to recognise that they are part of the HTML tag, it reads them as the end of the *string* of text that `echo` is trying to insert into the page. After that, it's looking for a semicolon (`;`) but instead it finds `t` and gets very confused! This kind of problem can come up quite often either because you've forgotten which kind of quotes to use or you're copying from another of your programs and used quotes differently there. Luckily, it's very easy to fix. Just replace the double quotes in the `input` tag with single quotes, like this!
```php
echo "Your guess: <input type='text' name='guess'/>";
```
5. Run the code again! Now you've got somewhere for your user to put their text! Type something in and press the enter key. Watch the page URL in the browser and notice what changes!