# DART ASSESSMENT

* This is a Dart assessment to create a script/algorithm that will catch an event and track it along various pointss on it's designated path and time it to see how       long it takes from user pressing the button to the thing actually happening.

/**
 * I created a button that when pressed, it returns a snackbar toast message and I had to track how long it takes for the toast message to show on screen after the        button has been pressed.
 
 * This class is where i created a Stateless Widget that will show a snackbar message after this onPressed function has been executed.

       class SnackBarPage extends StatelessWidget {
         const SnackBarPage({Key? key}) : super(key: key);

         @override
         Widget build(BuildContext context) {
           return Center(
             child: ElevatedButton(
               onPressed: () {

                 // Start the Stopwatch
                 final stopwatch = Stopwatch()..start();

                 final snackBar = SnackBar(
                   content: const Text('Yay! You pressed a button'),
                   action: SnackBarAction(
                     label: 'Undo',
                     onPressed: () {
                       // Some code to undo the change.
                     },
                   ),
                 );

                 // End the Stopwatch and print how long it took to return the snackbar message
                 print('pressButton() executed in ${stopwatch.elapsed}');

                 // Find the ScaffoldMessenger in the widget tree
                 // and use it to show a SnackBar.
                 ScaffoldMessenger.of(context).showSnackBar(snackBar);
               },
               child: const Text('ENTER'),
             ),
           );
         }
       }


 * I started the Stopwatch right after the onPressed function so that I can start tracking from this point.

      @override
      Widget build(BuildContext context) {
        return Center(
          child: ElevatedButton(
            onPressed: () {

              // Start the Stopwatch
              final stopwatch = Stopwatch()..start();

       * I stopped the Stopwatch right after the toast message is dispalyed and put a print statement to get the output results.

      final snackBar = SnackBar(
        content: const Text('Yay! You pressed a button'),
        action: SnackBarAction(
          label: 'Undo',
          onPressed: () {
            // Some code to undo the change.
          },
        ),
      );

      // End the Stopwatch and print how long it took to return the snackbar message
      print('pressButton() executed in ${stopwatch.elapsed}');

* THESE WERE MY RESULTS AFTER RUNNING THE PROGRAM 

      Restarted application in 170ms.
      Restarted application in 198ms.
      pressButton() executed in 0:00:00.000299
      Restarted application in 289ms.

