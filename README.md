# PythonBasic
## Python Home
```python
print("Hello, World!")
```
## Python Syntax 
들여쓰기는 코드 줄의 시작 부분에 있는 공백을 나타낸다
들여쓰기를 건너 뛰면 Python에서 오류가 발생한다.
```python
if 5 > 2:
  print("Five is greater than Two!")
```
동일한 코드 블록에서 동일한 수의 공백을 사용해야 한다.
```python
if 5 > 2:
  print("Five is greater than Two!")
if 10 > 5:
      print("Ten is greater than Five!!")
```
---
## Python Comments
- 파이썬 코드를 설명하는 데 사용할 수 있다
- 주석을 사용하여 코드를 더 읽기 쉽게 만들 수 있다
- 주석은 코드를 테스트할 때 실행을 방지하는 데 사용할 수 있다.

### 여러줄 주석
파이썬에는 여러 줄 주석에 대한 구문이 따로 없다.

여러 줄 주석을 추가하려면 각 줄에 대해 #을 삽입 해야한다.
```python
#This is a comment
#written in
#more than just on line

print("Hello, World!")
```
---
# Python Variables
## 변수 생성
파이썬에는 변수를 선언하는 명령이 없기 때문에 변수는 값을 처음 할당하는 순간 생성된다.
```python
x = 5
y = "Jae won"
print(x)
print(y)
```
변수는 특정 형식으로 선언할 필요가 없으며 설정된 후에도 형식을 변경할 수 있다.
```python
x = 4       # x is of type int
x = "Jae won" # x is now of type str
print(x)
```
## 데이터 변환
변수의 데이터 유형을 지정하려는 경우 캐스팅 기능을 사용하여 수행할 수 있다.
```python
x = str(3)    # x will be '3'
y = int(3)    # y will be 3
z = float(3)  # z will be 3.0
```
## 유형 가져오기
‘type()’ 함수를 사용하여 변수의 데이터 유형을 가져올 수 있다.
```python
x = 5
y = "Jae won"
print(type(x))
print(type(y))
```
## 작은 따옴표 & 큰 따옴표
문자열 변수는 작은 따옴표 또는 큰 따옴표를 사용하여 선언할 수 있다.
```python
x = "John"
# is the same as
x = 'John'
```
## 대소문자 구분
변수 이름은 대소문자를 구분한다
```python
a = 4
A = "Sally"
#A will not overwrite a
```
## 파이썬 변수 규칙
- 변수 이름은 문자 또는 밑줄 문자로 시작해야 한다
- 변수 이름은 숫자로 시작할 수 없다
- 변수 이름에는 영숫자와 밑줄(A-z, 0-9 및 _)만 사용할 수 있다
- 변수 이름은 대소문자를 구분한다(age, Age 및 AGE는 서로 다른 세 가지 변수다).
- 변수 이름은 Python 키워드일 수 없다.
```python
  myvar = "John"
my_var = "John"
_my_var = "John"
myVar = "John"
MYVAR = "John"
myvar2 = "John"
```
## 여러 단어 변수 이름
- 두 개 이상의 단어가 포함된 변수 이름은 읽기 어려울 수 있기 때문에 더 읽기 쉽게 만드는 데 사용할 수 있는 방법이 있다

**1) 캬멜 케이스(Camel Case)
-** 첫 번째 단어를 제외한 각 단어는 대문자로 시작한다

**2) 파스칼 케이스(Pascal Case)
-** 각 단어는 대문자로 시작한다

**3) 뱀 케이스(Pascal Case)
-** 각 단어는 밑줄 문자로 구분된다

## 여러 변수에 대한 많은 값 
```python
x, y, z = "Orange", "Banana", "Cherry"
print(x)
print(y)
print(z)
```
## 여러 변수에 대한 하나의 값
```python
x = y = z = "Orange"
print(x)
print(y)
print(z)
```
## 컬렉션 압축 풀기 
목록, 튜플 등에 값 모음이있는 경우. Python을 사용하면 값을 변수로 추출할 수 있다. 
이를 압축 풀기라고 한다
```python
fruits = ["apple", "banana", "cherry"]
x, y, z = fruits
print(x)
print(y)
print(z)
```
## 출력 변수
1) 변수를 출력하는 데 사용
```python
x = "Python is awesome"
print(x)
```
2) 함수에서 여러 쉼표로 구분된 변수
```python
x = "Python"
y = "is"
z = "awesome"
print(x, y, z)
```
3) 연산자를 사용하여 출력
```python
x = "Python "
y = "is "
z = "awesome"
print(x + y + z)
```
4) 숫자의 경우 문자는 수학 연산자로 작동
```python
x = 5
y = 10
print(x + y)
```
5) 함수에서 문자열과 숫자를 연산자와 결합하면 파이썬에서 오류 발생
```python
x = 5
y = "John"
print(x + y)
```
6) 함수에서 여러 변수를 출력하는 가장 좋은 방법은 쉼표로 구분하는것
```python
x = 5
y = "John"
print(x, y)
```
## 전역 변수
함수 외부에서 변수를 만들고 함수 내에서 사용
```python
x = "awesome"

def myfunc():
  print("Python is " + x)

myfunc()
```
함수 내에서 동일한 이름의 변수를 만들면 이 함수 내에서만 사용가능
```python
x = "awesome"

def myfunc():
  x = "fantastic"
  print("Python is " + x)

myfunc()

print("Python is " + x)
```
## Global 키워드
일반적으로 함수 내에서 변수를 만들 때는 local로 사용하며 해당 함수 내에서만 사용가능하다.
```python
def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)
```
- 함수 내에서 전역 변수를 변경하려는 경우
```python
x = "awesome"

def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)
```
<함수 외부에서 변수의 값을 지정하는 것: 전역변수>
<함수 내에서 변수의 값을 지정하는 것: global키워드>

---
# Python Data Types

문자열 유형:	`str`

숫자(정수,실수) 유형:	`int`, `float`, `complex`

시퀀스 유형:	`list`, `tuple`, `range`

매핑 유형:	`dict`

세트 유형:	`set`,`frozenset`

부울 유형:	`bool`

바이너리 유형:	`bytes`, `bytearray`, `memoryview`

없음 유형:	`NoneType`

1. **텍스트 유형 (Text Type)**:
    - 문자열(string)과 같은 텍스트 데이터를 다루는 데 사용됩니다.
    - 예시: "Hello, World!", "Python is awesome!"
2. **숫자 형식 (Numeric Types)**:
    - 숫자 데이터를 다루는 데 사용됩니다.
    - 정수형(integers), 부동 소수점형(floats), 복소수형(complex numbers)을 포함합니다.
    - 예시: 10, 3.14, 2 + 3j
3. **시퀀스 유형 (Sequence Types)**:
    - 순서가 있는 데이터의 집합을 다루는 데 사용됩니다.
    - 문자열(string), 리스트(list), 튜플(tuple) 등이 포함됩니다.
    - 예시: "Hello", [1, 2, 3], (1, 2, 3)
4. **매핑 유형 (Mapping Types)**:
    - 키-값(key-value) 쌍의 집합을 다루는 데 사용됩니다.
    - 딕셔너리(dictionary)가 대표적인 예시입니다.
    - 예시: {"name": "John", "age": 30}
5. **세트 유형 (Set Types)**:
    - 고유한 값들의 집합을 다루는 데 사용됩니다.
    - 중복된 값을 허용하지 않습니다.
    - 집합 연산(합집합, 교집합 등)을 지원합니다.
    - 예시: {1, 2, 3}
6. **부울 유형 (Boolean Type)**:
    - 논리적인 참(True)과 거짓(False)을 나타내는 데 사용됩니다.
    - 주로 조건문과 논리 연산에서 활용됩니다.
    - 예시: True, False
7. **바이너리 유형 (Binary Type)**:
    - 이진 데이터(binary data)를 다루는 데 사용됩니다.
    - 파일 입출력과 네트워크 통신에서 주로 사용됩니다.
    - 예시: 바이너리 파일 데이터

## 데이터 형식 가져오기
아래 함수를 사용하여 모든 개체의 데이터 형식을 가져올 수 있다.
```python
x = 5
print(type(x))
```
# Python Numbers

## 파이썬 숫자
- 파이썬에는 세 가지 숫자 유형이 있다
int, float, complex
- 숫자 유형의 변수는 값을 할당할 때 생성된다
  ```python
  x = 1    # int
  y = 2.8  # float
  z = 1j   # complex
  ```
- 파이썬에서 객체의 유형을 확인하려면 type()함수를 사용하면 된다.
  ```python
  print(type(x))
  print(type(y))
  print(type(z))
  ```
## 정수
```python
  x = 1
y = 35656222554887711
z = -3255522

print(type(x))
print(type(y))
print(type(z))
```
## 실수
```python
x = 1.10
y = 1.0
z = -35.59

print(type(x))
print(type(y))
print(type(z))
```
## 컴플렉스
```python
x = 3+5j
y = 5j
z = -5j

print(type(x))
print(type(y))
print(type(z))
```
## 형식변환
```python
x = 1    # int
y = 2.8  # float
z = 1j   # complex

#convert from int to float:
a = float(x)

#convert from float to int:
b = int(y)

#convert from int to complex:
c = complex(x)

print(a)
print(b)
print(c)

print(type(a))
print(type(b))
print(type(c))
```
## 난수
import random

print(random.randrange(1, 10))
---
# Python Casting

## 변수 유형 지정
- 변수에 유형을 지정하려는 경우 캐스팅으로 수행할 수 있다.
- 파이썬에서의 캐스팅은 생성자 함수를 사용하여 수행한다.

- int()

정수 리터럴, float 리터럴에서 정수를 생성합니다
( all decimals) 또는 문자열 리터럴(문자열이 정수를 나타내는 경우)
```python
x = int(1)   # x will be 1
y = int(2.8) # y will be 2
z = int("3") # z will be 3
```
float()

정수 리터럴, float 리터럴 또는 문자열 리터럴에서 float 숫자를 생성합니다(문자열이 float 또는 정수를 나타내는 경우).
```python
x = float(1)     # x will be 1.0
y = float(2.8)   # y will be 2.8
z = float("3")   # z will be 3.0
w = float("4.2") # w will be 4.2
```
str()

문자열, 정수 리터럴 및 float 리터럴을 포함한 다양한 데이터 유형에서 문자열을 생성합니다.
```python
x = str("s1") # x will be 's1'
y = str(2)    # y will be '2'
z = str(3.0)  # z will be '3.0'
```

# Python Strings

## 문자열
- 파이썬의 문자열은 작은따옴표 또는 큰따옴표로 묶여있다.
- ‘hello’ = “hello”
```python
print("Hello")
print('Hello')
```

## 변수에 문자열 할당
```python
a = "Hello"
print(a)
```

## 여러 줄 문자열
```python
a = """Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua."""
print(a)
```
```python
a = '''Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua.'''
print(a)
```

## 문자열은 배열로 인식
- 파이썬에는 문자 데이터 유형이 없으며 단일 문자는 단순히 길이가 1인 문자열이다
- 첫 번째 문자 위치는 0이다.
```python
a = "Hello, World!"
print(a[1])
```

## 문자열 루핑
```python
for x in "banana":
  print(x)
```

## 그렇지 않은지 확인
특정 구문이나 문자가 문자열에 없는지 확인하려면 다음을 사용할 수 있습니다. 
```python
txt = "The best things in life are free!"
print("expensive" not in txt)
```

## 슬라이싱
slice 구문을 사용하여 문자 범위를 반환할 수 있습니다.

시작 인덱스와 끝 인덱스를 콜론으로 구분하여 지정하여 문자열의 일부입니다.

```python
b = "Hello, World!"
print(b[2:5])
```

## 네거티브 인덱싱
음수 인덱스를 사용하여 문자열의 끝에서 조각을 시작합니다.
```python
b = "Hello, World!"
print(b[-5:-2])
```
---

# Python Booleans

## 부울 
프로그래밍에서는 표현식이 인지 또는 인지 알아야 하는 경우가 많습니다.`TrueFalse`

Python에서 모든 표현식을 평가하고 다음 두 가지 중 하나를 얻을 수 있습니다. 
답변 또는 .`TrueFalse`

두 값을 비교하면 표현식이 평가되고 Python은 부울 대답
```python
print(10 > 9)
print(10 == 9)
print(10 < 9)
```
if 문에서 조건을 실행하면 Python은 또는 다음을 반환합니다.TrueFalse

```python
a = 200
b = 33

if b > a:
  print("b is greater than a")
else:
  print("b is not greater than a")
```

## 함수 -> 부울
Boolean Value를 반환하는 함수를 만들 수 있습니다.
```python
def myFunction() :
  return True

print(myFunction())
```
---
# Python Operators

## 연산자
Python은 연산자를 다음 그룹으로 나눕니다.

- 산술 연산자
- 대입 연산자
- 비교 연산자
- 논리 연산자
- ID 연산자
- 멤버 자격 연산자
- 비트 연산자
---

# Python Lists
```python
mylist = ["apple", "banana", "cherry"]
```

## 목록
```python
thislist = ["apple", "banana", "cherry"]
print(thislist)
```

## 목록 길이
```python
thislist = ["apple", "banana", "cherry"]
print(len(thislist))
```

## 목록 항목 - 데이터 형식
```python
list1 = ["apple", "banana", "cherry"]
list2 = [1, 5, 7, 9, 3]
list3 = [True, False, False]
```
```python
list1 = ["abc", 34, True, 40, "male"]
```
---
# Python Tuples
```python
mytuple = ("apple", "banana", "cherry")
```

## 튜플

튜플은 단일 변수에 여러 항목을 저장하는 데 사용됩니다.

Tuple은 컬렉션을 저장하는 데 사용되는 
Python의 4가지 내장 데이터 유형 중 하나입니다. 

data, 나머지 3개는 List, Set 및 Dictionary이며 모두 품질과 사용법이 다릅니다.

튜플은 순서가 지정되고 변경할 수 없는 컬렉션입니다.

튜플은 둥근 대괄호로 작성됩니다.
```python
thistuple = ("apple", "banana", "cherry")
print(thistuple)
```
---
# Python Sets
```python
myset = {"apple", "banana", "cherry"}
```
## 집합
집합은 단일 변수에 여러 항목을 저장하는 데 사용됩니다.

Set은 컬렉션을 저장하는 데 사용되는 
Python의 4가지 내장 데이터 유형 중 하나입니다. 
data, 다른 3개는 List, Tuple 및 Dictionary이며 모두 품질과 사용법이 다릅니다.

집합은 순서가 지정되지 않고, 변경할 수 없으며 인덱싱 되지 않은 컬렉션이다.

집합은 중괄호로 작성됩니다.
```python
thisset = {"apple", "banana", "cherry"}
print(thisset)
```
---
# Python Dictionaries
```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
```
## 사전
사전은 데이터 값을 키:값 쌍으로 저장하는 데 사용됩니다.

딕셔너리는 순서가 지정되고, 변경 가능하고, 변경되지 않는 컬렉션입니다. 
중복을 허용합니다.

딕셔너리는 중괄호로 작성되며 키와 값이 있습니다.
```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict)
```
---
# Python If...Else

## 파이썬 조건과 if문
파이썬은 수학의 일반적인 논리 조건을 지원합니다.

- 같음: a == b
- 같지 않음: a != b
- 보다 작음: a < b
- 작거나 같음: a <= b
- 보다 큼: a > b
- 크거나 같음: a >= b
```python
a = 33
b = 200
if b > a:
  print("b is greater than a")
```
## 엘리프
```python
a = 33
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
```
## 다른
```python
a = 200
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
else:
  print("a is greater than b")
```
## 약식
```python
if a > b: print("a is greater than b")
```
## 중첩 if
```python
x = 41

if x > 10:
  print("Above ten,")
  if x > 20:
    print("and also above 20!")
  else:
    print("but not above 20.")
```
## pass문
```python
a = 33
b = 200

if b > a:
  pass
```
---
# Python While Loops

## 파이썬 루프
파이썬에는 두 가지 기본 루프 명령이 있습니다.

- while 루프
- for 루프

## While루프
```python
i = 1
while i < 6:
  print(i)
  i += 1
```
## break문
```python
i = 1
while i < 6:
  print(i)
  if i == 3:
    break
  i += 1
```
## continue문
```
i = 0
while i < 6:
  i += 1
  if i == 3:
    continue
  print(i)
```
---
# Python For Loops

## 파이썬 For 루프
for 루프는 시퀀스 (즉, 목록, 튜플, 딕셔너리, 집합 또는 문자열).

이것은 다른 프로그래밍 언어의 for 키워드와 비슷하지 않으며 
다른 객체 지향 프로그래밍 언어에서 볼 수 있는 
반복자 메서드와 더 비슷하게 작동합니다.

for 루프를 사용하면 목록, 튜플, 집합 등의 각 항목에 대해 
한 번씩 일련의 명령문을 실행할 수 있습니다.
```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)
```
---
