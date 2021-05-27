# Python standardizations

Please follow these rules to the best of your ability when submiting a new .py or .pyi file.

* Name folders, files, any non-constant variables, and functions with lowercase snake case.
* Name global constants with uppercase snake case.
* Name classes and exceptions with capitalized camel case.
* Use absolute imports.
* Use 'from' import first, then a space, then regular imports.
* Oreder imports alphabetically.
* You are allowed to import classes, functions, and variables, but only if it saves you a significant amount of space (i.e. 'datetime.datetime', etc...)
* Import multiple things where possible in 'from' imports.
* Import typing directly.
* You may use '\*' imports if you are actually importing everything from a package, and the package has >5 elements.
* Use """s for docstrings, not "s or #s.
* Use google-style docstrings for everything, however consult the existing code for full formatting.
* Document that generators are returned, not the value that is yielded.
* Document 'Args:' with "arg name (arg type): arg description."
* Add docstrings above class variables, not regular variables.
* Use the full import paths to classes, functions, etc.. in docstrings (i.e. 'typing.List[discord.User]', 'core.module_importer.importables.Importer', etc...)
* Use typing to type-hint everything except variables and class variables.
* Use the value inside of args or kwargs for docstrings (i.e. 'args (str): The arguments.', 'kwargs (int): The configuration for this class.', etc...)
* Always include None in the 'Returns:' section of the docstring for a function or class method if it returns None.
* Errors should mostly be raised from the top-level function, not functions that it calls, unless exceptions are excessively complex.
* Consult existing code for guidelines on Exceptions (i.e. TypeError("{var} must be of type {type}"), ValueError("{var} must be in range({min}, {max + 1})"), etc...)
* Put all constant variables in the 'constants.py' file for the project you are working on, in the proper sub-header, ordered alphabetically.
* You can use Enums, though only when it makes sense to (i.e. not as user input, etc...)
* When giving output use 's to surround small string outputs and "s to surround large string outputs, if it is a very short and standard output you don't have to surround it with quotes at all (i.e. AM, PM, 'Mar', 'Tue', "Compiling i/o port 300 on connector refusal.", etc...)
* Use "s exclusively for strings, never 's.
* Always use f-strings not %s, .format(), or similar, unless absolutely necessary.
* Use the minimal number of brackets while still keeping your code easy to read.
* Use "if len(x) == 0" instead of "if len(x)" or "if x".
* Use {} to define dicts and set() to define sets.
* Use private (\_\_) class variables and getter/setter methods almost exclusively.
* Always use 'self' or 'cls' as the first argument in class methods.
* Use "(cls: typing.Type\[T\]) -> T:" for '\@classmethod' usages.
* Never use abnormal spacing (i.e. in enumerations, etc...)
* Do not use docstrings to document values in enumerations.
* Optionally use "Meta" after class names for classes that are meant to be inherited or used as meta classes.
* Always initiate class variables in \_\_init\_\_ unless there are inheritance complications.
* Rarely use the '\@dataclasses.dataclass' decorator, as it does not allow for easy runtime errors, you are allowed to in some cases where you are storing user input.
* In the end your top priority should be making your code easily readable.
* For anything not covered above, default to [the Google Python formatting guidelines](https://google.github.io/styleguide/pyguide.html).
