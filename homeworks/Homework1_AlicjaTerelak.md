# Homework 1. - Alicja Terelak

**1.1.** Write a script (or function) that takes as an input two numbers `width` and `height` and prints a rectangle with specified size.

Examples:
- `width=5` and `height=4` should result in terminal output:

```
#####
#   #
#   #
#####
```

- `width=7` and `height=2` should result in terminal output:

```
#######
#######
```

- `width=1` and `height=1` should result in terminal output:

```
#
```


## Rozwiązanie:

#### Przykład 1


```python
height = 4
width = 5

def rectangle(height, width): 
    for k in range(0, height): 
        print ("") 
        for l in range(0, width): 
            if (k == 0 or k == height - 1 or l == 0 or l == width - 1) : 
                print("#", end = "") 
            else : 
                print(" ", end = "") 

rectangle(height, width)
```

    
    #####
    #   #
    #   #
    #####

#### Przykład 2


```python
height = 2
width = 7

def rectangle(height, width): 
    for k in range(0, height): 
        print ("") 
        for l in range(0, width): 
            if (k == 0 or k == height - 1 or l == 0 or l == width - 1) : 
                print("#", end = "") 
            else : 
                print(" ", end = "") 

rectangle(height, width)
```

    
    #######
    #######

#### Przykład 3


```python
height = 1
width = 1

def rectangle(height, width): 
    for k in range(0, height): 
        print ("") 
        for l in range(0, width): 
            if (k == 0 or k == height - 1 or l == 0 or l == width - 1) : 
                print("#", end = "") 
            else : 
                print(" ", end = "") 

rectangle(height, width)
```

    
    #


**1.2.** Sum all perfect squares (numbers that are equal to the square of other number – 1, 4, ..., 9, 16, 25, 36, 49, ..., 9801, 10000) in range between 0 and 10000.

## Rozwiązanie:


```python
a = 0
b = 10000

def perfect_squares(a, b): 
    ile = 0
    for k in range (a, b + 1): 
        l = 1; 
        while l * l <= k:
            if l * l == k: 
                ile = ile + 1
            l = l + 1
        k = k + 1
    return ile

def sum_squares(n = 1):
    return (n * (n + 1) * ((2 * n) + 1)) / 6

print("Liczba idealnych kwadratów z zakresu od " + str(a) + " do " + str(b) + " wynosi", str(perfect_squares(a, b)) + ", natomiast ich suma wynosi " + str(sum_squares(n = b)) + ".")
```

    Liczba idealnych kwadratów z zakresu od 0 do 10000 wynosi 100, natomiast ich suma wynosi 333383335000.0.
    

**1.3.** Write a script for setting an alarm, which ask users whether they are employed (yes / no) and whether they are currently on vacation (yes / no). User should answer typing either `Y` for yes or `N` for no. If user specify incorrect answer (anything that is not `Y` or `N`) program should warn user about incorrect answer and ask again.

The script output `True` if user is employed and not on vacation (because these are the circumstances under which you need to set an alarm). It should output `False` otherwise. Examples:

Examples:

- setting an alarm

```
> Are you employed? (Y/N):
> y
> Incorrect answer.
> Are you employed? (Y/N):
> Y
> Are you on vacation (Y/N):
> N
> True
```

- not setting an alarm

```
> Are you employed? (Y/N):
> N
> Are you on vacation (Y/N):
> N
> False
```

## Rozwiązanie:


```python
zatrudniony = True
wakacje = True

while zatrudniony == True:
    praca = input('Are you employed? (Y/N)')
    if praca == "Y":
        zatrudniony = True
        break
    if praca == "N":
        zatrudniony = False
        print("False")
        break
    else:
        print("Incorrect answer.")

while wakacje == True:
    odpoczynek = input("Are you on vacation? (Y/N)")
    if odpoczynek == "Y":
        wakacje = True
        print("True")
        break
    if odpoczynek == "N":
        wakacje = False
        print("False")
        break
    else:
        print("Incorrect answer.")
```

    Are you employed? (Y/N) Y
    Are you on vacation? (Y/N) U
    

    Incorrect answer.
    

    Are you on vacation? (Y/N) Y
    

    True
    
