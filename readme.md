## Testing

This is an exercise on exploring linters in python as part of the Secure Software Development course of the CS PgCert at the University of Essex Online. 

## Linting

### Question 1

*Run styleLint.py.*

*What happens when the code is run?*

I received this message "IndentationError: expected an indented block".

*Can you modify this code for a more favorable outcome?*

Yes. 

*What amendments have you made to the code?*

I corrected the indentations.

### Question 2

```pip install pylint```

*Run pylint on pylintTest.py*

*Can you correct each of the errors identified by pylint? Before correcting the code errors, save the pylintTest.py file with a new name (it will be needed again in the next question).*

I received this message: pylintTest.py:26:7: E0001: Missing parentheses in call to 'print'. Did you mean print(encoded)? (<unknown>, line 26) (syntax-error).

I can correct the error by adding parentheses around *encoded*.

### Question 3
```pip install flake8```

*Run flake8 on pylintTest.py*

*Review the errors returned. In what way does this error message differ from the error message returned by pylint?*

I received this message: pylintTest.py:26:7: E999 SyntaxError: invalid syntax.

The description of the error is different and less specific.

*Run flake8 on metricTest.py.*

*Can you correct each of the errors returned by flake8? What amendments have you made to the code?*

The messages I received are as follows:

metricTest.py:1:1: E265 block comment should start with '# '
metricTest.py:13:1: E302 expected 2 blank lines, found 0
metricTest.py:17:1: E302 expected 2 blank lines, found 1
metricTest.py:18:1: E128 continuation line under-indented for visual indent
metricTest.py:19:1: E128 continuation line under-indented for visual indent
metricTest.py:20:1: E128 continuation line under-indented for visual indent
metricTest.py:24:5: E303 too many blank lines (2)
metricTest.py:26:9: E225 missing whitespace around operator
metricTest.py:30:9: E225 missing whitespace around operator
metricTest.py:30:18: E225 missing whitespace around operator
metricTest.py:33:80: E501 line too long (84 > 79 characters)
metricTest.py:34:9: E225 missing whitespace around operator
metricTest.py:35:13: E225 missing whitespace around operator
metricTest.py:38:31: E231 missing whitespace after ','
metricTest.py:39:15: E225 missing whitespace around operator
metricTest.py:41:44: E231 missing whitespace after ','
metricTest.py:41:54: E231 missing whitespace after ','
metricTest.py:42:13: E128 continuation line under-indented for visual indent
metricTest.py:43:13: E128 continuation line under-indented for visual indent
metricTest.py:44:15: E225 missing whitespace around operator
metricTest.py:45:9: E115 expected an indented block (comment)
metricTest.py:47:13: E128 continuation line under-indented for visual indent
metricTest.py:53:25: E231 missing whitespace after ','
metricTest.py:62:18: E225 missing whitespace around operator
metricTest.py:64:15: E225 missing whitespace around operator
metricTest.py:65:21: E225 missing whitespace around operator
metricTest.py:67:1: E302 expected 2 blank lines, found 1
metricTest.py:73:18: E231 missing whitespace after ','
metricTest.py:74:13: E225 missing whitespace around operator
metricTest.py:81:18: E225 missing whitespace around operator
metricTest.py:84:28: W292 no newline at end of file

The amendments I did were:
- Adding indentation to functions and control statements.
- Adding indentation for continuation lines
- Adding function docstrings.
- Adding spaces around operators
- Adding spaces after commas.
- Adding double space before class and function definitions.
- Removing extra lines
- Removing trailing spaces
- Added a new line at the end of the file

### Question 4

```pip install mccabe```

*Run mccabe on sums.py. What is the result?*

The following code was using to get the results ```python -m mccabe sums.py```.

Result:

4:0: 'test_sum' 1
If 7 2

*Run mccabe on sums2.py. What is the result?*

The following code  to get the results ```python -m mccabe sums2.py```.

Result:

4:0: 'test_sum' 1
7:0: 'test_sum_tuple' 1
If 10 2

*What are the contributors to the cyclomatic complexity in each piece of code?*
The number of branches in the code determines the cyclomatic complexity. For example, in the 'test_sum' and 'test_sum_tuple' functions had only a single branch, so the cyclomatic complexity.

## Equivalence partitioning

### Instructions

Run equivalence.py in the Codio workspace - Testing with Python - which is an implementation of equivalence partitioning. This test partitions integers [-3,5] into equivalence classes based on lambda x, y: (x-y)%4 == 0.

### Output

{1, -3}

{2, -2}

{3, -1}

{0, 4}

-3 : {1, -3}

-2 : {2, -2}

-1 : {3, -1}

0 : {0, 4}

1 : {1, -3}

2 : {2, -2}

3 : {3, -1}

4 : {0, 4}

### Comments

Since there were no assertion errors in the output, this means that partition classes were derived correctly. In other words, members of each class satisfied the equivalence relation.






