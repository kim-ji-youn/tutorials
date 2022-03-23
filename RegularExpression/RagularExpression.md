## 파이썬의 re 모듈
* 파이썬에서는 정규표현식을 지원하는 기본 모듈 ```re```가 있다.

## 정규식 객체
* re 모듈엔 정규식 객체 라는 개념이 있다. 
* ```re.compile()``` 함수는 문자열 패턴을 컴파일하여 정규식 객체를 반환
* 어떤 정규식을 코드 내에서 여러 번 사용하고자 할 때 ```re.compile()``` 함수로 정규식 객체를 만들어 사용
* 또는 정규식이 복잡한 경우에도 ```re.compile()``` 함수를 사용
```
import re
text = "abcdefg"
pattern = re.compile("e")
print("정규식 객체의 자료형 : ", type(pattern))
print("정규식 객체 사용하는 경우 : ", pattern.findall(text))
print("객체를 사용하지 않는 경우 : ", re.findall("e", text))
```

## 정규식 검사 함수
문자열에 대해 정규식으로 검사하는 함수는 대표적으로 re.match(), re.search(), re.findall(), re.finditer()

* ```re.match(pattern, string)```	
    * ```string``` 시작 부분부터 패턴이 존재하는지 검사하여 **MatchObject**를 반환
* ```re.search(pattern, string)```	
    * ```string``` 전체에서 ```pattern```이 존재하는지 검사하여 **MatchObject**를 반환
* ```re.findall(pattern, string)```	
    * ```string``` 전체에서 패턴과 매치되는 모든 경우를 찾아 **list**로 반환
* ```re.finditer(pattern, string)```	
    * ```string``` 전체에서 패턴과 일치하는 결과에 대한 **iterater 객체**를 반환

## 문자열 수정 함수
re 모듈에는 패턴과 매치된 문자열을 찾아줄 뿐만 아니라, 편집할 수 있는 함수들도 존재

* ```re.sub(pattern, repl, string)```	
    * ```string``` 에서 ```pattern```과 매칭되는 부분을 ```repl```로 수정한 문자열을 반환
* ```re.subn(pattern, repl, string)```	
    * ```re.sub()```과 동일하지만, 함수의 결과를 ```(결과 문자열, 교체 횟수)```꼴의 튜플로 반환

## 메타 문자
* ^ :  검색하는 문자열 내에서 특정 문자(열)로 시작하는 경우에만 한정지어 매칭
    * 예를 들어, ```^ex```란 패턴은 문자열 앞에 ```"ex"```로 시작해야 매칭
    * 예시 : (expand, expire, extend, exclaim...)

* $ : 검색하는 문자열 내에서 특정 문자(열)로 끝나는 경우에만 한정지어 매칭
    * 예를 들어, ```ful$``` 은 문자열의 끝에 ```"ful"```이란 문자열이 등장하는 경우에 매칭
    * 예시 : (helpful, useful, wonderful...)

* | : 여러 가지의 문자열을 동시에 검색
```
>>> p3 = "apple|banana"             # apple 또는 banana가 포함되면 매치
>>> m3 = re.findall(p3, "I like apple and banana")
>>> print("m3 결과 : ", m3)
m3 결과 :  ['apple', 'banana']
```

* \[\] : 여러 조건을 만족하게 하는 방법
* \[^\] : not의 의미, \[\] 내부에 있는 문자열을 제외한 문자열을 검색
```
import re

p1 = "a|e|i|o|u"     # 알파벳 모음에 매치
p2 = "[aeiou]"     # 알파벳 모음에 매치
p3 = "[^aeiou]"     # 알파벳 모음이 아닌 문자(자음)에 매치

m1 = re.findall(p1, "Life is short, art is long")
m2 = re.findall(p2, "Life is short, art is long")
m3 = re.findall(p3, "Life is short, art is long")

print("m1 결과 : ", m1)
print("m2 결과 : ", m2)
print("m3 결과 : ", m3)

m1 결과 :  ['i', 'e', 'i', 'o', 'a', 'i', 'o']
m2 결과 :  ['i', 'e', 'i', 'o', 'a', 'i', 'o']
m3 결과 :  ['L', 'f', ' ', 's', ' ', 's', 'h', 'r', 't', ',', ' ', 'r', 't', ' ', 's', ' ', 'l', 'n', 'g']
```
