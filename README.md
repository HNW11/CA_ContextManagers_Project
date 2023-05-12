# CA_ContextManagers_Project
Code Academy Project on Context Managers


CODE ACADEMY OBJECTIVE 

Aisha's Greetings
You are a part of Aisha’s Greetings - a card printing company that prints greeting cards with a hint of personalization! You want to help Aisha create a system that generates cards based on customers’ requests.

You have been provided with two pre-filled card types:

happy_bday.txt: a card with a birthday message
thankyou_card.txt: a card file with a thank you message
Click through the files on your right and see what’s in them! If you get stuck, you can look at a sample solution of the project by looking at greetings_solutions.py - but try it out on your own first.

Let’s start printing!


First Step: 
Aisha, the owner of Aisha’s Greetings, wants to create a program that will automatically generate pre-filled orders, using her custom greeting messages.
Import the contextlib modules @contextmanager decorator, and create a decorated function named generic that takes in card type, sender’s name, and recipient arguments.

Second Step:
The generic() function will serve the purpose of opening a specific generic card type (Thank you card or Birthday card) so that it can be used as the base template for a more customized card.
        A variable to store a call of the open() built-in function that opens up a generic card type based on the card type parameter in read mode. You can assume the store will receive either a birthday card request or a thank you card request.  
        A variable to store a call of the open() built-in function that creates (and opens) a new card named with the following pattern: < sender_name >_generic.txt.

Third Step:
Now, you need to make sure the context manager correctly creates a customized card from the generic template. Inside the generic() context manager use the try clause to yield a file so that it creates the following template custom card:
        Dear < receiver >
        < text from the generic template card > 
        Sincerely, < sender >

Fourth Step:
Finally, make sure to close both files after usage!

Fifth Step:
It’s time for a test run! Aisha’s Greetings just got a customer ‘Mwenda’ who requested an order for a generic Thank you card for her friend ‘Amanda’.
        Use a with statement to generate this order. Have the with statement confirm the card is created by printing 'Card Generated!'.

Sixth Step:
We want to verify whether or not the correct order was printed in the file. Use a with statement to open and read the file you just created in the last step.

Seventh Step:
Aisha’s Greetings also wants to print personalized cards! This means that customers can tell Aisha’s Greetings the words they want in their card and we can print them.
        For personalized cards, let’s create a class-based context manager.

Eigth Step:
Next, write a __init__ method that takes the sender’s and receiver’s names and saves them as attributes.
        Add one more attribute that stores a newly opened (or created) file in write mode with the format < sender_name >_personalized.txt. This is the file we will be working on!

Ninth Step:
Now, let’s set up what should happen when any new files are created and the context is started.
        Make an __enter__ method that writes the receiver’s name to the opened file and returns that file. The format we write to the file should look like this: Dear < receiver>

Tenth Step:
Lastly, let’s set up the final pieces of the customized card.
        Create an __exit__ method that writes "Sincerely" followed by the sender’s name on the open file and then closes the file!
NOTE: There was no direction to do error handling so I just used *exec instead of all the arguments

Eleventh Step:
Time to give our custom card generator a test run!
        Aisha’s shop just got a customer 'John' who requested an order for a personalized card for his close friend 'Michael'.

Twelth Step:
Aisha’s Greetings just got two orders from a customer named 'Josiah'.  He wants to get a generic birthday card for a colleague named 'Remy' and a personalized card for his sister 'Esther'
        Create a nested with statement that generates these orders in one call.

Thirteenth Step:
Congrats! You were able to help Aisha’s Greetings create a system that generates cards quicker and smoother using the knowledge you gained about context managers!