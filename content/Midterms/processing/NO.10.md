# Variables
- variables are CASE SENSITIVE

- you must define variables **BEFORE** using them.

# Assigning values
- x = y; will result in the value of y overwriting the value of x.

- numbers like 10 or 4 are literals. this means that the value cannot be changed. Therefore, efforts to change the value by overwriting them with variables or other literals will not work.

# casting 
This happens when you define the value of a int to be a float or vice versa. The values will automatically be changed to the appropriate format. 
(floats will lose their decimal points when converted to integers)

- explicit casting: BIGGER -> SMALLER (you will lose detail)
  
- implicit casting: SMALLER ->BIGGER (done automatically in processing, gains detail)

# Others
- You can not define the same variable multiple times. THIS IS DIFFERENT from assigning another value to the variable after the fact.

- you can not define literals. 
  For example: 
 ```
  2 = 3 , 2 = a; //big no no
 ```

- Reserved keywords. there are a couple names that you cannot use as variables names. consult the [wiki](https://forum.processing.org/one/topic/reserved-keywords-wiki-page.html).for more information. 

[[NO.11]]