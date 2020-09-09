# DATA 531 - Programming for Data Science
# Lab 1: Python Functions, Lists, and Dictionaries

## Objectives

1. Create and call Python functions with parameters (including parameters with default values).
2. Use of Python built-in functions including math functions and functions in random package.
3. Mastery of list operations including traversing a list with a for loop, list indexing, and operations such as append.
4. Experience with use of dictionaries as a key-value data store.

## (Optional) Question #0 - Practice python syntax



## Question #1 - Creating and Calling Functions (10 marks)

Create a Python program that creates and calls a function for calculating the average of a list of values. Details:

- Put a comment at the top of the Python file called ``lab1q1`` with your name. (0.5 mark)
- Create function with name ``avglist`` that accepts three parameters: (1 mark)
    - ``lst`` - list of numbers
    - ``low`` - miminum value (not inclusive). Default = 0
    - ``high`` - maximum value (not inclusive). Default = 100
- Function will calculate and return the average of all values in the range (``low``, ``high``). (3 marks)
- Function should have a docstring as shown in output. (1 mark)
- Call ``help(avglist)`` to display function information. (0.5 marks)
- Create a list with the numbers 1 to 10 and call ``avglist()`` with default range and print result. (1 mark)
- Create a list with the numbers 1 to 100 and call ``avglist()`` with range (``20``, ``80``) and print result. (1 mark)
- Create a list with 100 random numbers between 1 and 100 and call avglist() with range (``30``, ``100``) and print the result. Note: Will need to ``import random`` and use ``random.randint(1,100)``. To set seed, use ``random.seed(0)``. (2 marks)

### Sample Output

    Help on function avglist in module __main__:

    avglist(lst, low=0, high=100)
    Returns average of a list of numbers in given range (low, high)
    
    Args:
       lst: list of numbers
       low: minimum value (not inclusive) Default: 0
       high: maximum value (not inclusive) Default: 100
       
    Return:
       Average of list of numbers

    Average of list from 1 to 10 (default range): 5.5
    Average of list from 1 to 100 range (20,80): 50.0
    Average of random list of 100 numbers from 1 to 100 and range (30,100): 62.41095890410959


## Question #2 - Using Lists (10 marks)

Create a Python program that performs list operations based on user input. Details:

- Put a comment at the top of the Python file called ``lab1q2`` with your name. (1 mark)
- Create a list with the numbers ``2, 4, 6, 8, and 10``. (1 mark)
- Using a while loop, prompt the user for an operation to perform until ``X`` for exit is selected. (1 mark)
    - If operation is ``A``, prompt for a number and append that number to the list. (1 mark)
    - If operation is ``P``, print the list. (1 mark)
    - If operation is ``G``, prompt for an index and print the number at that index from the list. Make sure it is a valid index otherwise print ``Error invalid index``. (2 marks)
    - If operation is ``D``, prompt for a number and delete that number from the list. (1 mark)
    - If operation is ``R``,  prompt for two numbers ``startIdx`` and ``endIdx`` and return a range from the list ``[startIdx, endIdx]``. Make sure it is a valid range otherwise print ``Error invalid index``. (2 marks)    
-  **Bonus:** If operation is ``S``, sort the list in ascending order. (1 mark) 
-  **Bonus:** Write a method that takes a list and index as a parameter and returns true if index is valid. (1 mark) 

### Sample Output

    Enter an operation: P
    [2, 4, 6, 8, 10]
    Enter an operation: A
    Enter number to add: 5
    Enter an operation: P
    [2, 4, 6, 8, 10, 5]
    Enter an operation: D
    Enter number to remove: 4
    Enter an operation: P
    [2, 6, 8, 10, 5]
    Enter an operation: G
    Enter index to get: 3
    Number at index 3 is 10
    Enter an operation: G
    Enter index to get: 5
    Error invalid index
    Enter an operation: R
    Enter start index: 2
    Enter end index: 4
    List range: [8, 10]
    Enter an operation: R
    Enter start index: 0
    Enter end index: 5
    Error invalid index
    Enter an operation: S
    Enter an operation: P
    [2, 5, 6, 8, 10]
    Enter an operation: X
   

## Question #3 - Letter Frequency Analysis using Dictionaries (5 marks)

Create a Python program that takes a string text and calculates the frequency of each letter and punctuation. Data set (copy as string into Python code):

    text = """She should have died hereafter.
    There would have been a time for such a word.
    Tomorrow, and tomorrow, and tomorrow,
    Creeps in this petty pace from day to day
    To the last syllable of recorded time,
    And all our yesterdays have lighted fools
    The way to dusty death. Out, out, brief candle!
    Life's but a walking shadow, a poor player
    That struts and frets his hour upon the stage
    And then is heard no more. It is a tale
    Told by an idiot, full of sound and fury,
    Signifying nothing.""" # Macbeth: Act 5, Scene 5, Page 2

Details:
- Put a comment at the top of the Python file called ``lab1q3`` with your name and copy data set above into Python code. (0.5 mark)
- Create an empty dictionary to store letter counts.  Upper and lower case letters should be counted together as upper case (e.g. 'A' and 'a'). Punction '.' and '!' and spaces (' ')  have their own entries. All other characters counted as '#' (for other). (0.5 mark)
    - Note that upper case letters are in ASCII table from 65 to 91 and lower case from 97 to 123. [ASCII Table](https://ascii.cl/) [Helpful info](https://terrameijar.wordpress.com/2017/02/03/python-how-to-generate-a-list-of-letters-in-the-alphabet/)
    - Note: ord() function may be useful.
- Use a for loop to process each letter in the text: (1 mark)
    - Use dictionary to update letter counts. Note: Will need to search dictionary to see if letter exists. If not, then add it otherwise add one to count. (2 marks)
- Output the total number of characters and for each character its count and frequency. (1 marks)   
-  **Bonus:** Read text data from file [``data.txt``](data.txt) instead of putting it in code. (1 mark)
-  **Bonus:** Sort output alphabetically. Hint: sorted() function. (1 mark)

### Sample Output

    Total characters: 477
    S 22 4.612159329140461
    H 21 4.40251572327044
    E 38 7.966457023060797
      78 16.352201257861637
    O 36 7.547169811320755
    U 14 2.9350104821802936
    L 18 3.7735849056603774
    D 25 5.241090146750524
    A 33 6.918238993710692
    V 3 0.6289308176100629
    I 19 3.9832285115303985
    R 26 5.450733752620545
    F 12 2.5157232704402515
    T 36 7.547169811320755
    . 5 1.0482180293501049
    # 21 4.40251572327044
    W 8 1.6771488469601676
    B 5 1.0482180293501049
    N 19 3.9832285115303985
    M 7 1.4675052410901468
    C 5 1.0482180293501049
    P 6 1.2578616352201257
    Y 12 2.5157232704402515
    G 6 1.2578616352201257
    ! 1 0.20964360587002095
    K 1 0.20964360587002095

    Bonus:
      78 	16%
    ! 1 	0%
    # 21 	4%
    . 5 	1%
    A 33 	7%
    B 5 	1%
    C 5 	1%
    D 25 	5%
    E 38 	8%
    F 12 	3%
    G 6 	1%
    H 21 	4%
    I 19 	4%
    K 1 	0%
    L 18 	4%
    M 7 	1%
    N 19 	4%
    O 36 	8%
    P 6 	1%
    R 26 	5%
    S 22 	5%
    T 36 	8%
    U 14 	3%
    V 3 	1%
    W 8 	2%
    Y 12 	3%
