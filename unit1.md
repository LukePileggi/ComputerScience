# Unit 1: A electronic hardware store

## Criteria A: Planning 

### Context of the problem
There is a hardware store in Karuizawa. This store is quite old, Like 1000 years old. The owner, Mr Sakamoto, wants to upgrade his accounting software, which at the moment is kept on paper. He would like to have a software application tha replaces the accounting book. Mr Sakamoto got a new Mac PC from his nephew, and we would like to use it.

### Justification of the solution
***Here we will write the design statement: what we will do, how, by when***
We want to create a text besed applictaton which provides the functonality for our hardware store. The app should provide us the record of p
urchases, categorisation of items, record of inventory, calculations of totals, and billing. We will develop the application with python because it id the software er are using in class at the moment. In comparisation to C++ or C, Python has a lean and simple programing syntax. In addition, Python has become the most popular programing language ofet the last few years. [1] Similaryly, Python hhas a large repository of libraries and documentation.

T.E.L.O.S study: Technology, Economic, Legal, Organisational, Scheduling

[1]Eastwood, B., 2020. The 10 Most Popular Programming Languages To Learn In 2020. [online] Northeastern University Graduate Programs. Available at: <https://www.northeastern.edu/graduate/blog/most-popular-programming-languages/> [Accessed 13 September 2020].

## Criteria for success
1. Provifes clear feedback to user (usibility)
1. **There are no bugs in the application**
1. The application should allow to calculate the total and begining
1. Secure application: It allows user login/authentication

## Criteria B: Design

### System diagram

### Flow diagram

### Record of tasks
| Task # | Planned action                                                                                        | Planned outcome                       | Time estimated | Target completion date | Criteria |
|--------|-------------------------------------------------------------------------------------------------------|---------------------------------------|----------------|------------------------|----------|
| 1      | Planning: Discuss the context of the situation. (Ideally this is the first interview with the client) | Write the context of the problem      | 15 min         | Sep 11                 | A        |
| 2      | Development: Coded the a text-based system for some parts in the hardware store.                      | A working program that shows the menu | 80 min         | Sep  18th              | D        |
| 3      |                                                                                                       |                                       |                |                        |          |

## Criteria C: Development

First test of text based menu:
```.py
welcome_msg = "Welcome to Sakamoto's store"
print(welcome_msg)
print("This is the menu")
print("=" * 20)
print('1. RAM $1')
print('2. CPU $5')
print('3. Motherboard $5')
print('4. GPU $2')
```

The following code is a dice simulation. It uses the random library.
```.py
counts =[0,0,0,0,0,0]

import random
for trial in range(1000):
    number = random.randint(0,60)
    if number < 10:
        counts[0] +=1
    elif 9 < number <20:
        counts[1] +=1
    elif 19 < number <30:
        counts[2] +=1
    elif 29 < number <40:
        counts[3] +=1
    elif 39 < number <50:
        counts[4] +=1
    elif 49 < number <60:
        counts[5] +=1

    for index, c in enumerate(counts):
    error = c - num_trial/6
    print("Number of {}s: {}, expected {}, error {}".format(index+1,c, num_trial/6, error))
```
![](https://github.com/LukePileggi/unit1/blob/master/Fig.2.Comp.Idea.jpg?raw=true)
This is an image tht shows what we think is inside the computer. We used our knowledge and research to make a good guess on each components' names and numbers.

The encryption code
```.py
# This code sorts each line & text in the file
import random
all_lines_of_db = open("database.txt", "r").readlines()
items = all_lines_of_db[0].strip().split(",")
prices = all_lines_of_db[1].strip().split(",")
amount = all_lines_of_db[2].strip().split(",")

# This part of the code encrypts the text in the file written above
for line in all_lines_of_db:
    encrypted_line = ""
    len_line = len(line)
    for letter in line:
        # The coder is a random number that hides the actual information
        coder = random.randint(-5,5)
        encrypted_letter = chr(ord(letter) + coder)
        encrypted_line += encrypted_letter
    print('line length: {}, encryption: {}'.format(len_line, encrypted_line))
    print("Decryption code:{}".format(coder))
```

## Criteria D: Functionality

## Criteria E: Evaluation

