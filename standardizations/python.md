# Python standardizations

Please follow these rules to the best of your ability when submiting a new .py or .pyi file.

* Use absolute imports.
* "from" imports come first, then regular imports, ordered by raw length of the import then alphabetically (if using "from" imports base it on the first package that you are actually importing, not the package that you are importing from).
* Make sure to order modules in "from" imports alphabetically.
* You are allowed to import classes, functions, and variables if it saves you a significant amount of space.
* You may use '*' imports if you are actually importing everything from a package, and the package has >5 modules.
* Use google-style docstrings for everything, however consult the existing code for full formatting.
* Document that generators are returned, not the value that is yielded.
* Document 'Args:' with "arg name (arg type): arg description."
* Add docstrings above class variables.
* Use """s for docstrings, not "s or #s.
* Use full import paths to classes, functions, etc.. in docstrings.
* Use typing to type-hint everything except variables, and class variables.
* Try to mostly import typing directly, not things from typing.
* Use the value inside of args or kwargs for docstrings (i.e. args (str), kwargs (int), etc...)
* Always include None in the Returns section of the docstring for a function or class method if it returns None.
* Consult the existing code for guidelines on Exceptions (i.e. TypeError("{var} must be of type {type}"), ValueError("{var} must be in range({min}, {max + 1})"), etc...)
* Errors should mostly be raised from the top-level function, not functions that it calls, unless exceptions are excessively complex.
* Put all constant variables in constants.py, in the proper sub-header, ordered alphabetically.
* You can use Enums, though only when it makes sense to (i.e. not as a command input, etc...)
* When giving output from commands use 's to surround small string outputs and "s to surround large string outputs, if it is a very short and standard output you don't have to surround it with quotes at all (i.e. AM, PM, 'Mar', 'Tue', "Compiling i/o port 300 on connector refusal." etc...)
* Use "s exclusively for strings, never 's.
* Always use f-strings not %s, .format(), etc.. unless absolutely necessary.
* Use the minimal number of brackets.
* Use {} to define dicts, set() to define sets.
* In the end you should try to make your code easily readable.
* Use private (\_\_) class variables and getter/setter methods almost exclusively.
* Always use "self" or "cls" as the first argument in class methods.
* Never use abnormal spacing (i.e. in enumerations, etc...)
* Do not use docstrings to document values in enumerations.
* Use "Meta" after class names for classes that are meant to be inherited or used as meta classes.
* Always initiate class variables in \_\_init\_\_ unless there are inheritance complications.
* Never use the @dataclass decorator, as it does not allow for easy runtime errors.
* Use "if len(x) == 0" instead of "if len(x)" or "if x".
* Import multiple things where possible in 'from' imports.
* Use "(cls: typing.Type\[T\]) -> T:" for '\@classmethod' usages.
* For anything not covered above, default to [the Google Python formatting guidelines](https://google.github.io/styleguide/pyguide.html).
