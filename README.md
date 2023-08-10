# AirBnB Clone
The AirBnb clone is a copy of the official AirBnB website
- incorporating a full web application
- with a command interpreter to handle data without a visual interface.
- This includes a web front-end that displays both static and dynamic data
- a database to store data
- an api that provides a communication interface between the frontend and the data.

## The console
- The console is a command line interpreter designed to help manage the data models and objects on the storage engine for the backend part of a website.
- It is capable of creating, updating, destroying objects, retrieving, storing and persisting objects to a JSON file, operating on objects (count, compute stats, etc...),
- updating attributes of an object.


## To start and use the console:
* Clone this repo: `git clone "https://github.com/Makish2023/AirBnB_clone.git"`
* Enter AirBnb_clone directory: `cd AirBnB_clone`
* To Run the console(interactively): enter `./console.py`
	- A prompt `(hbnb)` is displayed for input, then enter command. Example::memo:
		- (hbnb) `show <user>` : Prints the string representation of an instance based on the class name and id.
		- (hbnb) `EOF` : exits console
		- (hbnb) `create <class>` : Create an object (prints its id)
		- (hbnb) `all` or `all <class>` : Show all objects, or all instances of a class
	
* To Run hbnb(non-interactively): `echo "<command>" | ./console.py`. Example::memo:
	- `echo "help" | ./console.py`
		- It shows the lists of commands available. If you include a command you want help on,
		the output is more verbose and restricted to details of that command, when available.
	- `echo "count place" | ./console.py`
		- Retrieves the number of instances of a given class : place

Command | Example
------- | -------
Run the console | ```./console.py```
Quit the console | ```(hbnb) quit```
Display the help for a command | ```(hbnb) help <command>```
Create an object (prints its id)| ```(hbnb) create <class>```
Show an object | ```(hbnb) show <class> <id>``` or ```(hbnb) <class>.show(<id>)```
Destroy an object | ```(hbnb) destroy <class> <id>``` or ```(hbnb) <class>.destroy(<id>)```
Show all objects, or all instances of a class | ```(hbnb) all``` or ```(hbnb) all <class>```
Update an attribute of an object | ```(hbnb) update <class> <id> <attribute name> "<attribute value>"``` or ```(hbnb) <class>.update(<id>, <attribute name>, "<attribute value>")```

### A look of some examples, usage and behaviour on the terminal when run interactively:

$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) 
(hbnb) 
(hbnb) quit
$

### Non-interactive mode (example)

```bash
$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
```

## File Descriptions
[console.py](console.py) - the console contains the entry point of the command interpreter. 
List of commands this console current supports:
* `EOF` - exits console 
* `quit` - exits console
* `<emptyline>` - overwrites default emptyline method and does nothing
* `create` - Creates a new instance of`BaseModel`, saves it (to the JSON file) and prints the id
* `destroy` - Deletes an instance based on the class name and id (save the change into the JSON file). 
* `show` - Prints the string representation of an instance based on the class name and id.
* `all` - Prints all string representation of all instances based or not on the class name. 
* `update` - Updates an instance based on the class name and id by adding or updating attribute (save the change into the JSON file).

## Authors
Kevin Sagini Oroko - [Github](https://github.com/Makish2023) / [Twitter](https://twitter.com/SaginiKevin2)  

## License
Public Domain. No copyright protection. 

