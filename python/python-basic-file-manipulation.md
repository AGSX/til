# Basic Pig

**Date: June 1, 2016**

#### Introduction

Python is able to support file read and manipulation. The essential functions for file manipulation will be discussed.

#### File Open

```python
file_handler = open ('this_is_your_file.file_format')
```

#### File Close

```python
file_handler = open ('this_is_your_file.file_format')

# file manipulation logic must be here

file_handler.close()
```

Note: Don't forget to close.

#### File Read

```python
file_handler = open ('this_is_your_file.file_format')

# will get all the content from the file
file_content = file_hanlder.read()

# will get content of file line by line
file_content = file_hanlder.readline()

file_handler.close()
```

Note: The readline function will keep track which line the program is currently reading.

#### File Write

```python
file_handler = open ('this_is_your_file.file_format', 'w')
file_content = file_hanlder.write()
file_handler.close()
```

#### Truncate File Content

```python
file_handler = open ('this_is_your_file.file_format', 'w')
file_content = file_hanlder.truncate()
file_handler.close()
```

#### References

- [Learn Python the Hard Way](http://learnpythonthehardway.org/book/)

#### Author

Almer Mendoza
