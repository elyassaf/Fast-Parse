# Fast Parse - A fast way to get terminal arguments!

With Fast Parse, you can get command line and terminal arguments in an easy and convenient way. With only **one line of code**.

## Overview

The Fast Parse module provides the following features:

-   An easy way to get a basic command line or terminal arguments.
-   If the user doesn't give the arguments in the command line, they will need to give them through the input.

## Get Stared

-   [ ] First, you need to download it from pip. `pip install fastparse`

-   [ ] Then import it to your project.
``` python
from fastparse import fast_parse, try_parse
```

### fast_parse
This function is THE function. fast_parse enables you to get command lines arguments with one line of code, as following.
```python
args = fast_parse('all', 'of', 'your', 'command', 'line', 'arguemtns')

# later on you can get the argumetns from the 'args' variable
all_value = args.get('all')

print(all_value)
```

Now it's time to let the user add the arguemnts.
```shell
python main.py 'all_value_here' 'of_value_here' 'your_value_here', 'command_value_here', 'line_value_here', 'arguments_value_here'
```

The output is:

`all_value_here`

_Note: the fast_parse function returns a value (in the above example we called it 'args'), this value is a dictionary._


### try_parse
try_parse is a bit more exciting than fast_parse, it lets the user add the arguments in the command line and if they don't, it asks them to give the args in the input.

Let's look at an example,
```python
args = try_parse('arg1', 'arg2')

arg1_value = args.get('arg1')

print(arg1_value)
```

If we give the arguments in the terminal it works just as fast_parse
```shell
python main.py 'arg1_value_here' 'arg2_value_here'
```
Output is as expected: `arg1_value_here`

**But if we don't give the arguments in the command line, it asks the arguments in the input**

```shell
python main.py
enter arg1 value: arg1_value
enter arg2 value: arg2_value
```

And the output is: `arg2_value`
