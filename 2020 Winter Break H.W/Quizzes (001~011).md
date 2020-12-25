# 2020 Winter Break H.W_by Kien Le Trung
## Quizzes

### Quiz 001
#### Solution:
![](https://github.com/BrightChanges/Unit-2/blob/main/IMG_7854.JPG)

#### Flow Diagram:
![](https://github.com/BrightChanges/Unit-2/blob/main/IMG_9488.JPG)

#### Codes:
```.py

def Makes10(A,B):
    if (A==10 or B==10) or (A+B==10):
        return True
    return False


print("A,B in this test is 9,10 so this should show True; result=", Makes10(9,10))
print("A,B in this test is 1,9 so this should show True; result=",Makes10(1,9))
print("A,B in this test is 2,5 so this should show False; result=",Makes10(2,5))

```


#### Testing:
![](https://github.com/BrightChanges/Unit-2/blob/main/Screen%20Shot%200002-12-23%20at%2010.09.22%20PM.png)

### Quiz 002
#### Solution:
![](https://github.com/BrightChanges/Unit-2/blob/main/IMG_7167.JPG)

#### Flow Diagram:
![](https://github.com/BrightChanges/Unit-2/blob/main/IMG_3988%202.JPG)


#### Codes:
```.py

def IntMax(A,B,C):
    if A>B and A>C:
        return A
    elif B>A and B>C:
        return B
    elif C>A and C>B:
        return C

print("All results below should show 3")
print("result=",IntMax(1,2,3))
print("result=",IntMax(3,2,1))
print("result=",IntMax(1,3,2))

```

#### Testing:
![](https://github.com/BrightChanges/Unit-2/blob/main/Screen%20Shot%200002-12-23%20at%2010.36.01%20PM.png)

### Quiz 003
#### Solution:
![](https://github.com/BrightChanges/Unit-2/blob/main/IMG_5295.JPG)

#### Flow Diagram:
![](https://github.com/BrightChanges/Unit-2/blob/main/IMG_2822.JPG)

#### Codes:
```.py

def rangeN(N):
    sum=0
    for x in range(N+1):
        sum += x
        print("All integers from 0 to {} is:".format(N),x)

    return "Sum of those integers is", sum


test1=6
test2=8
test3=10

print(rangeN(test1))
print(rangeN(test2))
print(rangeN(test3))

```


#### Testing:
![](https://github.com/BrightChanges/Unit-2/blob/main/Screen%20Shot%200002-12-23%20at%2010.54.35%20PM.png)


### Quiz 004
#### Solution:
![](https://github.com/BrightChanges/Unit-2/blob/main/IMG_9927.JPG)

#### Flow Diagram:
![](https://github.com/BrightChanges/Unit-2/blob/main/IMG_6494.JPG)

#### Codes:
```.py

def perfectN(N):
    sum = 0
    print("Integer entered is", N)
    for i in range(1,N-1):
        if N%i == 0:
            print(i)
            sum+=i
    if sum==N:
        print("Sum of factor is:", sum)
        return True
    return False

print(perfectN(6))
print(perfectN(50))

```


#### Testing:
![](https://github.com/BrightChanges/Unit-2/blob/main/Screen%20Shot%200002-12-25%20at%206.31.05%20PM.png)

### Quiz 005

#### Solution:
![](https://github.com/BrightChanges/Unit-2/blob/main/IMG_5012.JPG)

#### Flow Diagram:
![](https://github.com/BrightChanges/Unit-2/blob/main/IMG_7852.JPG)

#### Codes:
```.py

def tableM(N):
    print("The integer N entered is", N)
    for i in range(1,10):
        print(N, "x ", i, "=", N*i)


print(tableM(2))

```


#### Testing:
![](https://github.com/BrightChanges/Unit-2/blob/main/Screen%20Shot%200002-12-25%20at%206.49.42%20PM.png)

### Quiz 006

#### Solution:
![](https://github.com/BrightChanges/Unit-2/blob/main/IMG_5550.JPG)

#### Flow Diagram:
![](https://github.com/BrightChanges/Unit-2/blob/main/IMG_6731.JPG)

#### Codes:
```.py

def MixStart(S):
    print("The entered string is:", S)
    if S[1]=="i" and S[2]=="x":
        return True
    return False

print(MixStart("mix snacks"))
print(MixStart("pix snacks"))
print(MixStart("piz snacks"))

```

#### Testing:
![](https://github.com/BrightChanges/Unit-2/blob/main/Screen%20Shot%200002-12-25%20at%206.59.04%20PM.png)
