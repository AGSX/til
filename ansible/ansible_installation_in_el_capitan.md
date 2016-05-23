# Ansible OS X El Capitan Installation issues

**Date: May 20,2016**

When running Ansible on OS X El Capitan, users will encounter "ERROR! Unexpected Exception: (setuptools 1.1.6 (/System/Library/Frameworks/Python.framework/Versions/2.7/Extras/lib/python), Requirement.parse('setuptools>=11.3'))" error.

To fix this issue, try to run this command:
```
"pip install --upgrade setuptools --user python"
```
