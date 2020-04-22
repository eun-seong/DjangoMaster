# 생활코딩 강의3
## 객체
* `class` 키워드를 이용하여 클래스를 선언   
* `pass` : 비어 있는 클래스를 만들 때 사용   
### 생성자
`__init__(self, val...)` 함수를 사용   
* `self` : `this`와 비슷한 느낌의 인수   
생성자 함수의 첫 번째 인수는 항상 자기 자신이다. 통상적으로 `self` 이름 사용한다.   
`self.valName`으로 지정한 `valName`이 객체의 변수가 된다.
```python
class Cal(object):
  def __init__(self, v1, v2):
    self.v1 = v1 
    self.v2 = v2 

  def add(self):
    return self.v1 + self.v2 

  def subtract(self):
    return self.v1 - self.v2 

c1 = Cal(50,30)
c1.add()      # 출력 : 80
c1.subtract() # 출력 : 20
```
## 캡슐화
당연한 내용인데 잊고 있었다.   
다시 제대로 생각하자!!    
* getter/setter 생성하기   
* 변수의 값을 받을 때 타입 오류 없는지 확인      
`isinstance(val, type)` : `val`이 `type`타입인지 체크   
+ public 변수를 `property`라고 함   
* 변수 이름 앞에 `__`를 붙이면 해당 클래스 이름과 함께 맹글링된다.   
=> _ClassName__method 식으로  
* 변수 이름 앞에 `_`를 붙이면 private 비슷하게 사용할 수 있다.   
하지만 인스턴스에서 직접 접근이 가능하다고 한다.   
```python
class C(object):
  def __init__(self, v):
    self.__value = v 
  def show(self):
    print(self.__value)

c1.show()
print(c1.__value)    # 에러
```
## 상속
class의 object 자리에 상속할 클래스의 이름을 넣으면 됨   
```python
class(Cal):
  def multiply(self):
    return self.v1*sefl.v2 
```
* 상속받은 클래스에 생성자가 없을 경우 부모의 생성자 실행    
* 부모의 인스턴스 그대로 받아옴   
## 클래스 멤버
* 인스턴스 : 로컬 변수    
* 클래스 메소드 : 인스턴스와 상관없이 동작하는 함수   
### 클래스 메소드 
* static method   
  - `@staticmethod` 어노테이션 사용   
  - 하위 클래스에서 실행할 경우 부모 클래스의 클래스 속성을 가져옴   
* class method   
  - `@classmethod` 어노테이션 사용   
  - 하위 클래스에서 실행할 경우 해당 인스턴스 클래스 속성을 가져옴   
  - 첫 번째 인자로 클래스를 가르키는 변수를 넣어줘야 함   
```python
@classmethod 
def getcount(cls):
  return C.count
```
* instatnce method   
인스턴스의 메소드   
## 클래스 변수 
* 클래스의 공통 변수   
인스턴스 마다 가지지 않고 한 클래스에서 공유하며 사용   
선언할 땐 함수들 위에 해야 함   
## 오버라이드  
부모 객체에 있는 메소드를 재정의하는 것    
* `super()` : 자식 클래스에서 부모 클래스   
이것을 이용하여 자식 클래스에서 부모 클래스의 메소드와 함께 사용할 수 있음   
## 다중 상속 
여러 개의 부모 클래스를 가질 수 있음   
```python
class C3(C1, C2):
  ... 
```
* `class.__mro__` : 상속에서 우선 순위를 보여줌    

### 단점 
자식 클래스를 선언할 때 상속을 받은 순서에 따라 중복되는 메소드가 실행될 수도 안될 수도 있다.   

