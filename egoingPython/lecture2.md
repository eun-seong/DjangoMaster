# 생활코딩 강의2
## 컨테이너
배열을 '리스트'라고 부름
* type 확인 : `type('string')`
--> <class 'str'>
### 리스트
배열과 비슷   
타입이 다른 원소들이 들어갈 수 있음
```python
print(type(['a', 'b', 'c'])) # 출력 | <class 'list'>
valList = ['a', 'b', 'c']
valList[1]  # 인덱스 접근 가능
```
`list.append()`     : push_back
'del(list[index])'  : 원소 삭제
## 반복문
### while문
```python
while True:
    어쩌고 저쩌고
```
### for문
```python
list = ['egoing', 'leezche', 'graphittie']
for element in list:
    print(element)
```
`range(a,b)`    : [a,b) 까지 실행
## 함수
### 함수 선언
```python
def function_name(val1, val2):
    어쩌고
    저쩌고
    return 리턴값
```
## 모듈
외부에서 가져오는 파일들
```python
import math
... 
# myModule에서 function_name의 함수만 import  
from myModule import function_name
funtion_name()

# myModule에서 function_name의 함수를 z로 가져옴
from myModule import function_name as z
z()

# 모듈 안의 모든 것 import
import myModule
myModule.function()

# myModule 모듈을 k로 사용
import myModule as k
k.function()
```

