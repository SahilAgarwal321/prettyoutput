[![N|Solid](https://www.python.org/static/community_logos/python-powered-w-100x40.png)](https://www.python.org/)
PrettyOutput allows you to print pretty colors with ease. What more do you want?

## Installation
Options:
1. Clone this repository (you probably know what you're doing)
2. Download the archive from releases

# Usage
```py
from utils import prettyoutput


prettyoutput.info(string='Well, isn\'t this neat?')
prettyoutput.success(string='Yes! Yes it is.')
prettyoutput.error(string='Oh noes!')
prettyoutput.warning(string='Get outta here!')
custom_message = prettyoutput.custom(string='Oh noes!', color_code='cyan', stat_msg='[MSG]', prn_out=False)
print(custom_message)
```
Notice how we created a custom message and stored the value to a variable? PrettyOutput allows you to circumvent implicitely printing your message so that you can do it yourself when you're ready.
### PrettyOutput also supports printing without args!
```py
import prettyoutput

prettyoutput.info()
prettyoutput.success()
prettyoutput.error()
prettyoutput.warning()
```
Notice when executed, everything is aligned perfectly!

## Got the time? We do!
Here's how to use the time option. All times are UTC.
```py
import prettyoutput

prettyoutput.error(time=True)
```
`[ERROR][2017-04-03/23:58:22]  | An error has ocurred!`
>Find yourself using `time` a lot? You should use `space` for all statuses, as well. This will automatically align
>all statuses so that `time` doesn't throw off the flow of your output!
```py
import prettyoutput

prettyoutput.error(time=True, space=True)
prettyoutput.info(time=False, space=True)
```
```
[ERROR][2017-04-04/00:10:52]  | An error has ocurred!
[INFO]                        | Information:
```

### Python interpreter acting funny?
You're probably seeing a really confusing string of characters, right?
```py
>>> import prettyoutput
>>> prettyoutput.error()
[ERROR]   | An error has occured!
'\x1b[0;31;40m[ERROR]   | \x1b[1;37;40mAn error has occured!'
>>>
```
Not to worry!
### Try this;
```py
>>> import prettyoutput
>>> print(prettyoutput.error(prn_out=False))
[ERROR]   | An error has occured!```
```
> PrettyOutput returns the message created so that it may be re-used.
> Save the returned string to a variable, and you may never have to call
> PrettyOutput again!

License
----

[![DUB](https://img.shields.io/dub/l/vibe-d.svg)](https://github.com/Aareon/Tipsy/blob/master/LICENSE)
