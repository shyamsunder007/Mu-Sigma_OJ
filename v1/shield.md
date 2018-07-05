# Shield

Shield is an extremely simple mechanism to forbid running of potentially harmful codes.

Shield is not a sandboxing solution. Shield provides only a partial protection against trivial attacks. Real protection against untrusted code comes only by enabling [Sandbox](sandboxing.md).

## Shield for Python

By enabling Shield for Python, Online Judge just adds some code at the beginning of submitted Python code before running to prevent using dangerous functions. These codes are located in files `tester/shield/shield_py2.py` and `tester/shield/shield_py3.py`.

You can enable/disable Shield for Python in Settings.

There are ways to escape from Shield in python and use blacklisted functions!

```python
# @file shield_py3.py

import sys
sys.modules['os']=None

BLACKLIST = [
  #'__import__', # deny importing modules
  'eval', # eval is evil
  'open',
  'file',
  'exec',
  'execfile',
  'compile',
  'reload',
  #'input'
  ]
for func in BLACKLIST:
  if func in __builtins__.__dict__:
    del __builtins__.__dict__[func]
```
