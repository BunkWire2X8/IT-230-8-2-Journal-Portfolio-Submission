# IT-230 : 8-2 Journal: Portfolio Submission

## Briefly summarize the requirements and goals of the application you developed.
To present class names in a graphical list, and then submit them to another list when selected. There is also redundancy and overdraw checking.

## What user needs was this application designed to address?
Technically, this doesn't really solve any "needs" due to be it being not technically functional. Hypothetically though, if this was reworked to be connected to something larger, it would allow ease of IT class registration for students applying to SNHU. Would be weird to have to download a program to do so, but yeah, that's the gist of it.

## What did you do particularly well in developing this application?
Error checking, detailed error messages, dictionary/array instantiating, and dictionary/array cycling.

## Compare and contrast the Console and WPF application designs. What screens and features were necessary to support user needs and produce a user-centered UI for the app? How did your UI designs keep users in mind? Why were your designs successful?
Neither of these designs were designed by _me_, as I was just following specifications. I can explain their functionality though.

### Console:
The console app displays a text-based list, and expects an input from the user. Once a valid input is received, it displays the input selected and as well as the past valid input before asking the user if they want to submit another. If it is redundant, overdrawn in credit hours, or has an unrecognized class number, it displays an appropriate error message and does not save the input.

### WPF Application:
Similar design philosophy to the console. It has a drop-down list for the inputs, and pressing a button will add it to a box listing the currently registered classes. The error/confirmation messages are displayed in a label above the box listing. The total credit hours is also displayed in its own text box, which is a slight improvement over the console application, as that one only informed you of the total credit hours when you attempted to overdraw.

## How did you approach the process of debugging and coding your application? What techniques or strategies did you use?
Well, I examined the code, saw what was missing, and implemented what I needed to, and rewrote other things to suit more efficient design principles. The console one has its fair share of code comments of what I fixed/added, such as improving boolean logic, replacing certain numbers with enums, and storing the list of classes in a dictionary. The latter was largely absent in things to fix, due to being much more barebones, but the code speaks for itself though really.

## How could you use those techniques or strategies in the future?
I have been using these techniques, and will likely continue to, in my own projects. Been working on making a custom addon for the Godot game engine, and it has involved processing numerous dictionaries and arrays. I also use my fair share of enums to make the code more readable. There's also a fair bit of boolean processing to make sure that certain code only executes when it needs to, and that values are applied appropriately.

## Where did you have to be innovative to overcome a challenge in the full application development process?
The dictionary in the console application simplified a lot of the logic once implemented. I could determine if an input was valid simply with `classListings.ContainsKey(choice)`, and easily get each class's name from the input with `classListings[choice]`. As for the WPF Application, I used a few boolean operators to simplify the error processing code and inform the user if there were two errors at once. Not as notable, but I couldn't really think of much else.
