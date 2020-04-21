# 생활코딩 강의1
### 출력
```python
print("Hello world!")
print('Hello "world"')  # 출력 : Hello "world"
```
- 큰 따옴표 : 텍스트   
- 작은 따옴표 : 기호, 식별자   
- 큰 따옴표 3개 : 정규표현식   
큰 따옴표 & 작은 따옴표 거의 완전히 같음   
따옴표 안에 다른 따옴표가 있어도 문자로 인식함   
## math library
```python
math.ceil()     # 올림
math.floor()    # 내림
math.pow(2, 10) # 지수
math.pi         # 파이 상수
```
## 문자열
### 문자열 제어
* 문자열 연산
```python
print('Hello '+'world')   # 문자열 + 연산 가능
print('Hello ' *3)        # 숫자만큼 반복해서 출력
print('Hello'[0])         # 인덱스 접근 가능
```
* 문자열 제어
```python
'문자열'.capitalize()       # 첫 글자만 대문자로
'문자열'.upper()            # 모두 대문자로
'문자열'.__len__()          # 문자열의 길이
len('문자열')               # 문자열의 길이
'문자열'.replace('A', 'B')  # '문자열'에서 'A'를 'B'로 변경
```
### 특수 문자들
* 탈출 문자   : \   
* 개행        : \n   
* 탭          : \t   
* 기본 경고음 : \a   
## 변수
### 변수 선언
```python
x = 10  # 타입 지정해주지 않음
```
## 조건문
참    : True   
거짓  : False   
```python
if True:
    print("참")
elif False:
    print("거짓")
else: 
    print('나머지')

```
## 입력과 출력
* 사용자 입력
```python
val = input("입력 : ")
```
## 논리 연산자
OR 연산   `or`   
AND 연산  `and`   
NOT 연산  `not`
# 비교 연산자
같다      `==` || `is`
같지 않다 `!=` || `not`
```python
not 1 is 1.0
# 출력 | True 
```






