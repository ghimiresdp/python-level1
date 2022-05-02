- **created by**: Sudip Ghimire
- **URL**: https://www.sudipghimire.com.np
- **Github**: https://github.com/ghimiresdp

**Table of Contents**
- [14.3. The `re` module](#143-the-re-module)
  - [`re.compile()` function](#recompile-function)
  - [`re.search()` function](#research-function)
  - [`re.match()` function](#rematch-function)
  - [`re.findall()` function](#refindall-function)
  - [`re.split()` function](#resplit-function)
  - [`re.sub()` function](#resub-function)

# 14.3. The `re` module

This chapter covers some examples of the regular expression using `re` module. If you're not reviewed
regular expressions and regex special characters, please review them first.

- [Chapter 14.1 Regular Expressions](chapter%2014.1%20regular%20expressions.md)
- [Chapter 14.2 Regex Special Characters](chapter%2014.2%20regex%20special%20characters.md)

or you can look at the official documentation from https://docs.python.org/3/library/re.html.


The `re` module contains several functions that helps finding out, compiling and matching regular expressions. Some of the functions are as follows:

## `re.compile()` function

The `re.compile()` function compiles the regular expression from the regular string. takes 2 arguments:
- `pattern`: a regular expression as a string
- `flags`: a value that can be specified to modify default behavior. _defaults to 0_
- The function returns a `re.Pattern` object which can then be used to match, search, or find all occurrences with that pattern.

**Example**: A regular expression that extracts the name of a country that starts with A and ends with a
```python
import re
countries = ['USA', 'Japan', 'Angola', 'China', 'Algeria', 'Nepal', 'Argentina', 'Albania']

pattern = re.compile(r'^A\w*a$')

```
The above pattern when matched with the list of countries should give matches for _Angola_, _Algeria_, _Argentina_ and _Albania_

```python
countries = ['USA', 'Japan', 'Angola', 'China', 'Algeria', 'Nepal', 'Argentina', 'Albania']

# a word that starts with A and ends with a
pattern = re.compile(r'^A\w*a$')

for country in countries:
    print(pattern.match(country))

# Output
"""
None
None
<re.Match object; span=(0, 6), match='Angola'>
None
<re.Match object; span=(0, 7), match='Algeria'>
None
<re.Match object; span=(0, 9), match='Argentina'>
<re.Match object; span=(0, 7), match='Albania'>
"""
```

## `re.search()` function
## `re.match()` function
## `re.findall()` function
## `re.split()` function
## `re.sub()` function