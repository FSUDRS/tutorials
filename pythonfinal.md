# Beginner's Python

## Introduction

Python is a programming language that is easy to get started with. There are many reasons to start with using Python, but a few of them are

* It's an object-oriented programming language
* It's high level (it reads more like human language than computer language)
* It works well with many different types of data \(e.g.  any plaintext data, including text, csv, json, xml, etc.\)
* It's popular, so lots of tools modules and libraries have already been created for it.

To get started we're going to go to [DHbox](http://dhbox.org), log in, and navigate to the Command Line tab. From the command line tab, we can run python by typing in `python3` and hitting enter. Python should be running now. To execute commands in Python, you must hit the enter \(return\) on the keyboard after typing in the command. If at any time you need to exit Python, press the Ctrl + z keys simultaneously to return to the Command Line.

## Variables
One of the first things to understand is the concept of a variable. A variable is an entity with an assigned name that you can use to store data and call on later in a program. To create a variable in Python, write the variable name followed by `=` \(the equal sign here is called the assignment operator\) and finally the value that you want to assign to the variable. The syntax to do this is:
`variable_name =[insert variable here]`. For example:


`Test =123`


The three most basic data types that you should know about before getting started are integers \(e.g. 1, 30004, \-24\), floating points \(e.g. 1.0, \-27.000485, 275000.01\), and strings \(e.g. “Library”, “The rain in Spain falls mainly on the plain.”, “375”\). Integers are whole numbers, with no decimal point, either positive or negative. Floating points contain a decimal point.Strings are always surrounded by either single \(‘I am a string.’\) or double quotation marks \(“I am also a string.”\).


When creating variable names in Python, some rules must be observed. Variable names must begin with either a letter or an underscore. The rest of the variable name can consist of letters, numbers and underscores \(no other special characters can be used\). Another consideration to make is that variable names are case sensitive \(i.e. libraryname, Libraryname, libraryName, and LIBRARYNAME would be four different variables\).

## Lists

Now that we’ve seen the three basic data types, we can use them to create other, more complex data types. The first new data type that we’ll create is a list. A list is precisely that: a list! The syntax or way to write a list is:


`[“every”, “list”, “object”, “is”, “separated”, “by”, “a”, “comma”]`


`[4, 8, 15, 16, 23, 42]`


`[“the”, “answer”, “to”, “life”, “the”, “universe”, “and”, “everything”, “is”, 42]`


Note that the final list contains strings as well as an integer. This is permissible in Python. Just as with the other data types \(strings, integers, and floating points\), lists can be assigned to a variable. Try assigning each of the lists above a variable name. Then call the list by typing in the variable name and pressing enter. 


Even though we've already created the lists, we can still add new items to the end of the list with the `.append` command. Use `list_variable_name.append("new list item")` to do this. We can also ask for individual items from a list by typing `list_variable_name[0]`. List items count up from zero, so the first item in the list will be called by using `[0]` while `[1]` refers to the second item in the list. We can also ask for the data type of a specific list item by typing the following command with the number of the item we want from the list `type(list_variable_name[0])`. If the result is a string, Python will return `<class 'str'>`, for an integer `<class 'int'>`, and `<class 'float'>` for a floating point.

## Dictionaries

Now let's make yet another data type called a dictionary. Items in a dictionary are called *key: value pairs*. Keys must be unique strings within the dictionary. Look at the following example:


`wizard_info ={"name": "Harry Potter", "education": "Hogwarts", "address": "Cupboard Under the Stairs, 4 Privet Drive, Little Whinging, Surrey"}`


In the above example the strings “name”, “education”, and “address” are the keys in the *key: value pair* and the strings “Harry Potter” and “Hogwarts” are the values in the *key: value pair*. `wizard_info` is a variable name for this dictionary data type.


Dictionaries are different from lists in that the items they contain are not in a specific order, so commands such as the ones we used earlier to get specific items from a list will not work in a dictionary. You can write items to or overwrite items in the dictionary by calling the specific key and using the assignment operator `=` to declare a new value. For the dictionary above, writing in `wizard_info["education"]= "Florida State University"` will change Harry Potter's `"education"` info to `"Florida State University"` by overwriting `"Hogwarts"`.


## For Loops

Next, let's explore the use of *for loops* in Python. While it might not be so bad to rewrite a single line of code two or three times, imagine having to do so 500 times! *For loops* allow you to perform the same task over and over again, on lists, dictionaries, or other data types. For example, we can create the following list:


`drs_team =["Micah", "Devin", "Matt", "Rachel", "Sarah"]`


And now we'll operate a *for loop* on it:


```
for team_member in drs_team:

  print(team_member)
```

The result should be  alist of all the names from the original list. You will notice that we never created a variable called `team_member` before creating our *for loop*. However, Python creates a temporary variable called `team_member` and it is automatically used.


Now, let's try another loop on a dictionary instead of a list. Try entering the following data:


`hurricanes = {"Arlene": "Tropical Storm", "Bret": "Tropical Storm", "Cindy": "Tropical Storm", "Don": "Tropical Storm", "Emily": "Tropical Storm", "Franklin": "Category 1", "Gert": "Category 2", "Harvey": "Category 4", "Irma": "Category 5", "Jose": "Category 1", "Katia": "Category 2", "Lee": "Tropical Storm", "Maria": "Category 5"}`


Now, we'll operate a *for loop* on it:


`for name, strength in hurricanes.items(): print(name + " is a " + strength)`


What's happening above? `hurricanes.items()` is telling the dictionary to create a list of *key: value pairs*. `name` is on the left of the comma and `strength` is on the right. This tells Python that the key is being assigned to the variable `name` and the value is being assigned to the variable `strength`. If you entered everything correctly, the result should come back with each of the hurricanes listed in the following format:


`Katia is a Category 2`


Before moving on, let's look at `if`, `else`, and `elif` statements. Else/if statements are a way to say, "If \(if\) this condition exists, execute this code. If this condition doesn't exist \(else\), execute this other code." Try out the example below \(When entering the code below, be careful to indent the lines as they are shown. If you don't properly indent the code, it will not execute. Use two spaces at the beginning of indented lines as you see them below.):

```
x =10
if x > 9:
  print("This number is more than 9!")
else:
  print("This number is 9 or less.")
```

When you hit enter to execute the program, it should return `This number is more than 9!` because 10 > 9. If you rewrite the code above but change the value of x to a number less than 10 the `else` section of the code willecute:


```
x =3
if x > 9:
  print("This number is more than 9!")
else:
  print("This number is 9 or less.")
```


Now, the result is `This number is 9 or less`.


Sometimes we want more than two possible end results, though. This is where `elif` comes in handy. You can string together as many `elif` statements as you want between an `if` and an `else` statement. Try out the following example:


```
drs_team =["Micah", "Devin", "Matt", "Rachel", "Sarah"]
if drs_team[0] == "Micah":
  print(drs_team[0] + " is the director.")
elif drs_team[0] == "Sarah":
  print(drs_team[0] + " is leading this workshop.")
else:
  print(drs_team[0] + " is a really good colleague.")
```


Since the value `"Micah"`  is the first value in the list, only the `if` statement will execute. However, by changing the order of items in the list, you can probably figure out how you would get the `elif` and `else` parts of the code to exectue instead. One thing that we haven't seen yet is `==`. This is different from the assignment operator `=`. `==` checks to see if the value on the left is equal to the value on the right \(in much the same way as `>` and `<` check whether the value on the left is greater than or less than the value on the right\).


Finally, let's combine the *for loop* and `if`, `else`, and `elif` statements. Try out the following example and be sure to pay attention to punctuation and indentation!


```
for team_member in drs_team:
  if team_member == "Micah":
    print(team_member + " is the director.")
  elif team_member == "Sarah":
    print(team_member + " is leading this workshop.")
  else:
    print(team_member + " is a really good colleague.")
```


The result should look something like:


```
Micah is the director.
Devin is a really good colleague.
Matt is a really good colleague.
Rachel is a really good colleague.
Sarah is leading this workshop.
```

## Conclusion


These are the very basic steps to getting started programming in Python.