# QwuikLib *(pronounced quick-lib)*
is a Python terminal utility library that adds useful functions for CLI programs.

## About
QwuikLib is a library that adds terminal utility functions such as `typewrite()` or `summarize()`.

These functions aren't general purpose and all do their own specific task.

Every function has docstrings, alongside a GitHub wiki page.

## Installation
`pip install qwuiklib`
## Dependencies
None! It currently only uses the `random` and `time` libraries, and you don't need to import either - that's handled by the library itself.

Got me thinking, if you import a library that imports a library... would you be able to use the functions from the library imported by the library? Okay, no, I'm making no sense.
## Example functions
### `typewrite(text: str = "Hello World!", delay: float = 0.02, punc_matters: bool = False, punc_del_mult: float = 2.0)`
<details><summary>Docstring</summary>
Typewriter effect for your terminal.
Prints each character of a string with a customisable delay.

text (str): The string you want to print. May be multiline or single-line. Default: "Hello World!"

delay (float): The delay (in seconds) that you want the programme to wait between characters. Default: 0.02

punc_matters (bool): Whether or not you want to apply a modifier to the delay after a punctuation character. Default: False

punc_del_mult (float): The modifier that you want the delay to multiply by after a punctuation character. Only works if punc_matters is True. Default: 2.0
</details>

### `summarize(iterable=[1,2,3], skip_strings: bool = True, convert_numerals: bool = False)`
<details><summary>Docstring</summary>
sum() only supports floats and integers? Wow, how pathetic.
Returns the sum of any iterable.
The function only adds integers, floats and strings to the sum.
String addition is dependent on the 2 boolean arguments.
Nested lists are not included in the summary.

iterable (any iterable type):
Accepts any iterable type, but reasonably only useful for lists and sets.
Though, it can also sum up all the numbers in a range.

skip_strings (bool):
If True, skip strings and only care about integers and floats.
If False, add the length of the string to the summary.

convert_numerals (bool):
Only works if skip_strings is False.
If the string is only numbers, convert it into an integer.
If it has a dot at any point into it, convert it into a floating point number.
</details>
