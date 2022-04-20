# dart-assesment
Dart Assessment


This is a Dart assessment to create a script/algorithm that will catch an event and track it along various pointss on it's designated path and time it to see how long it takes from user pressing the button to the thing actually happening.

# I USED A DART STOPWATCH TO CALCULATE HOW LONG IT TAKES FOR THE SNACKBAR MESSAGE TO SHOW AFTER YOU PRESS THE ENTER BUTTON

I created a button that when pressed, it returns a snackbar toast message.
I created an Elevated Button and after the onPressed function I put the stopwatch to begin tracking the time right after the button is pressed.
          
           // Start the Stopwatch
           final stopwatch = Stopwatch()..start();
 
I started the Stopwatch start time when the button is pressed and stopped the Stopwatch when the snackbar message is displayed to print how long it takes for the action to be executed

          // End the Stopwatch and print how long it took to return the snackbar message
          print('pressButton() executed in ${stopwatch.elapsed}');
          
# THESE WERE MY RESULTS 

Restarted application in 170ms.
Restarted application in 198ms.
pressButton() executed in 0:00:00.000299
Restarted application in 289ms.
