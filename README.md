# AppliedCSWithAndroidUnit1-Anagrams

This is the first project from Google's Applied CS with Android Course. Spec taken from course website:


The mechanics of the game are as follows:

The game provides the user with a word from the dictionary.
The user tries to create as many words as possible that contain all the letters of the given word plus one additional letter. Note that adding the extra letter at the beginning or the end without reordering the other letters is not valid. For example, if the game picks the word 'ore' as a starter, the user might guess 'rose' or 'zero' but not 'sore'.
The user can give up and see the words that they did not guess.
In order to ensure that the game is not too difficult, the computer will only propose words that have at least 5 possible valid anagrams.

Tour of the code

The starter code is composed of two java classes:

AnagramsActivity: In Android development an Activity is a single, focused thing that the user can do. Most of our apps in this class will have a single activity but often apps are made up of multiple activities (e.g. login, settings, etc.). The starter code implements several methods:
onCreate: this method gets called by the system when the app is launched. It is made up of some boilerplate code plus code that open the word list to initialize the dictionary and code to connect the text box to the processWord helper.
processWord: a helper that adds words to the UI and colors them
onCreateOptionsMenu: boilerplate
onOptionsItemSelected: boilerplate
defaultAction: this is the handler that is called when the floating button is clicked. Depending on the game mode, it either starts the game or shows the missing answer to the previous game.
AnagramDictionary: This class will store the valid words from the text file and handle selecting and checking words for the game. This is where your code will among the following methods:
AnagramDictionary: The constructor. It should store the words in the appropriate data structures (details below).
isGoodWord: Asserts that the given word is in the dictionary and isn't formed by adding a letter to the start or end of the base word.
getAnagrams: Creates a list of all possible anagrams of a given word.
getAnagramsWithOneMoreLetter: Creates a list of all possible words that can be formed by adding one letter to the given word.
pickGoodStarterWord: Randomly selects a word with at least the desired number of anagrams.
