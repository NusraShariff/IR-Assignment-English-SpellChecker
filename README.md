STUDENT DETAILS:
Name: Nusra Shariff
Roll No: S20230010167
Course: Information Retrieval(IR)
Assignment: English Spell Checker System

1. PROJECT OVERVIEW
This project implements a Spell Checker System that detects and corrects misspelled words in English sentences.
It uses the concept of Minimum Edit Distance to suggest the most similar words from a dictionary.
The system works for:
English (English dictionary)
It reads a sentence, identifies incorrect words, provides the best possible suggestions, and saves results in an output file.

2. MODULE DESCRIPTIONS
The project is organized into four main Java modules, each handling a specific task:

SpellChecker.java:
Handles user interaction, reads sentences, and loops for new input. It cleans each word (removes punctuation, converts to lowercase), checks if it exists in the dictionary, and if not, calls the suggestion module. It then prints the results and uses FileManager to save them.

DictionaryBuilder.java:
Reads the English dictionary file from the /data folder. It trims whitespace and converts every word to lowercase, storing them in a HashSet for fast, case-insensitive lookup.

EditDistance.java:
Implements the Minimum Edit Distance Algorithm to compute similarity between the misspelled word and dictionary words, returning the closest matches as suggestions.

FileManager.java:
Handles saving of program outputs (detected misspellings and their suggestions) into /output/test_results.txt.


4. SOFTWARE REQUIREMENTS
Operating System: Windows / Linux / macOS
Editor: Visual Studio Code
Language: Java
JDK Version: Java 17 or above

Check Java installation:
java -version
javac -version


5. HOW TO RUN THE CODE (IN VISUAL STUDIO CODE)

Step 1️: Open the Project
-Launch VS Code
-Go to File → Open Folder → select your project folder 

Step 2️: Create Folders
-If they don't already exist, create the `bin` and `output` folders in your main project directory.
- Make sure your `english_dictionary.txt` file is inside the `data` folder.

Step 3️: Compile the Java Source Files
-Open the built-in terminal in VS Code 
-Type the following command and press Enter. This tells the Java compiler (`javac`) to take all files from the `src` folder (`-cp src src/*.java`) and place the compiled `.class` files into the `bin` folder (`-d bin`).
    javac -d bin -cp src src/*.java

Step 4️: Run the Program
-In the same terminal, type the following command and press Enter. This tells Java (`java`) to look for class files in the `bin` folder (`-cp bin`) and run the main class `SpellChecker`.
    java -cp bin SpellChecker

Step 5️: Use the Spell Checker
-The program will load the dictionary and prompt you to:
    `Enter a sentence (or 'q' to quit):`
-Type any sentence (e.g., `hello worled`) and press Enter.
-The program will show you the misspelled words and their suggestions directly in the terminal.

Step 6️: Check the Saved Output
-After you test a sentence, open the `output` folder.
- You will find a file named `english_spell_check_results.txt` containing a log of all the misspellings and suggestions.

6. TEST CASES 

Here are 5 test cases used to verify the system, formatted as (Misspelled -> Corrected).

1.  "I receievd your mail"
    Misspelled: receievd
    Suggestion: recieved

3.  "Hello Worled"
    Misspelled: Worled
    Suggestion: World

5.  "this is tets cases"
    Misspelled: tets
    Suggestion: test

7.  "i helpd you"
    Misspelled: helpd
    Suggestion: helped
    
9.  "you are very sucesful"
    Misspelled: sucesful
    Suggestion: successful

