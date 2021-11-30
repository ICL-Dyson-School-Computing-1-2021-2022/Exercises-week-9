# Week-9-Exercises
Exercises for Week 9 of Computing 1 for the Dyson School of Design Engineering at Imperial College London.

## Building on the Resistor Class

1. Return to the Resistor Class you wrote in Week 8-1. You probably want to copy the file into this folder and edit it separately from the version you wrote last week. 

2. Move the the resistor colour code dictionary from being a local variable inside a function to being a class attribute. Do the same with the dictionary of the tolerance colours - remove it from the min and max methods and make it a class attribute. 

3. Update the methods that use those dictionaries so that they now refer to the class attributes instead of local variables. You can test if it works correctly by printing the attribute directly:

'''
import resistor as r
print(r.Resistor.resist_colours)
print (r.Resistor.tol_colours)
'''

## Simple Classes with Inheritance
1. Create a new file in this week's exercises folder called `icl_student.py`. Within it implement a class called `ImperialStudent` with the below instance attributes that have to be set at instantiation (e.g. `my_student = ImperialStudent('Alice Gast', 12345678)`):

    * name (string)
    * cid (integer)

2. Add a method to the `ImperialStudent` class called `can_get_book()` that returns whether a student can check out a book from the library which just always returns `True`.

3. Within the same file, implement a second class that extends `ImperialStudent`. Call it `DEStudent` and require the same input arguments as `ImperialStudent`, calling the `__init__()` of `ImperialStudent` to set those parameters. Also give it the addional instance attributes which are required as input parameters in the constructor:

    * year (integer, 1-4)
    * tutor (string)

4. Within the `DEStudent` constructor, create an additional instance attribute called `ace_induction` which is set to `False`.

5. Give the `DEStudent` a class attribute of

    * faculty (set to `'engineering'`)

6. Add a method only to the `DEStudent` class called `completed_ace_induction()` that sets the instance attribute `ace_induction` to `True`.

7. Verify in the Python shell that an instance of a `DEStudent` class can access book the library and workshop methods, but that an `ImperialStudent` can't access the workshop method.


## TFIDF Exercise Part 2: Inverse Document Frequency
*This is a more advanced exercise than will be required on the assessment, this is just a chance to challenge yourself if you are feeling comfortable with the content so far.*

1. Copy your Python file `tf_document.py` from Week 8 into this week's folder, in the same directory as this README. 

2. Open the Python file `tfidf_corpus.py` and complete the methods.

3. You can now query the corpus, for instance asking for the top 3 words for `mercutio.txt`.

```
>>> import tfidf_corpus as ti
>>> my_ti = ti.TFIDFCorpus('./text-files')
>>> my_ti.get_top_words('mercutio.txt', n=3)
['dream', "o'er", 'then']
```


