#### pythagoreanTheorem(length_a, length_b)
````
def pythagoremTheorem(length_a, length_b):
   sqLength_a = length_a * length_a
   sqLength_b = length_b * length_b
   sqLength_c = sqLength_a + sqLength_b
   length_c = math.sqrt(sqLength_c)
   return length_c
````
Example Outputs: 
````
 hypot = pythagoremTheorem(5,7)
````
   8.602325267042627

````
  hypot = pythagoremTheorem(4,9)
````
9.848857801796104
````
hypot = pythagoremTheorem(10,7)
````
12.206555615733702

#### list_mangler(list_in)
````
def list_mangler(list_in):
    newList =[]
    for num in list_in:
        if iseven(num):
            num = num *2
            newList.append(num)
        else:
            num = num * 3
            newList.append(num)
    return newList
````
My Function uses: 
````
def iseven(num):
    if num % 2 == 0:
        return True
    else:
        return False
````
Description: 

My function runs a for loop through the list and checks to see if the number is even or odd using my function iseven. If the number is even, I multiply it by 2 and add it to my new list. Similarly if the number is odd, I multiply it by 3 and add it to my list.

Example Outputs: 
 ```` 
c = [1, 2, 3 ,4,5, 6, 7, 8]
newList = list_mangler(c)
````
[3, 4, 9, 8, 15, 12, 21, 16]

````
c = [20, 222, 22, 400, 2]
newList = list_mangler(c)
````
[40, 444, 44, 800, 4]

````
c = [21, 23, 9, 401, 3]
newList = list_mangler(c)
````
[63, 69, 27, 1203, 9]

#### grade_calc(grades_in, to_drop)

````
def grade_calc(grades_in ,to_drop):
    grades_in.sort()
    grades_in.reverse()
    while to_drop != 0:
        num = grades_in[-1]
        grades_in.remove(num)
        to_drop = to_drop-1
    average = getAverage(grades_in)
    letterGrade = letterGrader(average)
    return letterGrade
````
My function uses: 
````
def getAverage(grades_in):
    sum = 0
    for value in grades_in:
        sum = sum + value
    average = 0
    average = sum / len(grades_in)
    return average
````
and 
````

def letterGrader(average):
    letterGrade = ''
    if average >= 90:
       letterGrade = 'A'
    elif average >= 80:
        letterGrade ='B'
    elif average >= 70:
        letterGrade = 'C'
    elif average >= 60:
        letterGrade = 'D'
    else:
        letterGrade ='F'
    return letterGrade
 ````
Description: 

My Function takes a lists and sorts it. Then it reverses the list order so that the smallest grades are at the end of the list. It then goes into a while loop in which it removes the last item from my list and continues until to_drop equals zero. It then averages the remaining list ( using getAverage) and assigns it to a letter grade using letterGrader.

Example Outputs: 

````
c = [100, 100, 90, 98,30]
grade = grade_calc(c, 2)
````
A

````
 c = [100, 10, 50, 40,30]
 grade = grade_calc(c, 2)
````
D

````
c = [100,20, 40, 75, 80, 10, 75, 40,30]
grade = grade_calc(c, 4)
````
C

#### odd_even_filter(numbers)
````
def odd_even_filter(numbers):
    evenList= []
    oddList = []
    for num in numbers:
        if iseven(num):
            evenList.append(num)
        else:
            oddList.append(num)

    return evenList, oddList
````
My code also uses: 

````
def iseven(num):
    if num % 2 == 0:
        return True
    else:
        return False
````
Description:

This code takes a list of numbers and, using a for loop, sorts them based on whether they are even or odd (using is even). It then adds the number to a evenList or Oddlist. 


Example Outputs: 

````
d = [100, 199, 200, 45]
    even, odd = odd_even_filter(d)
````
Even = [100, 200] Odd = [199, 45]
````
d = [1,2,3,4,5,6,7,8,9,10]
even, odd = odd_even_filter(d)
````
Even =[2, 4, 6, 8, 10] Odd= [1, 3, 5, 7, 9]

````
d = []
even, odd = odd_even_filter(d)
````
Even =[] Odd= []