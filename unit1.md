# Unit 1: A electronic hardware store

## Criteria A: Planning 

### Context of the problem
There is a hardware store in Karuizawa. This store is quite old, Like 1000 years old. The owner, Mr Sakamoto, wants to upgrade his accounting software, which at the moment is kept on paper. He would like to have a software application tha replaces the accounting book. Mr Sakamoto got a new Mac PC from his nephew, and we would like to use it.

### Justification of the solution
***Here we will write the design statement: what we will do, how, by when***

## Development

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
