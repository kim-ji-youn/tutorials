**[Programmers]의 [파이썬을 파이썬답게] 수업을 정리한 것입니다.**

[Programmers]: https://programmers.co.kr/
[파이썬을 파이썬답게]: https://programmers.co.kr/learn/courses/4008


#### 1. Introduction
```
def solution(mylist) :
  answer = []
  for i in mylist :
    answer.append(len(i))
  return answer
```
내가 짠 코드랑 똑같아서 소름.....
아래와 같이 짜는 것이 이 강의의 목표이다. 

```
def solution(mylist) :
  return list(map(len, mylist))
```


#### 2. 정수 다루기
##### 2-1. 몫과 나머지: [divmod]
  * \*: unpacking
  * divmod(x, y): (몫, 나머지)를 return 한다. 
##### 2-2. n진법으로 표기된 string을 10진법 숫자로 변환하기: [int 함수]
  * string\[::-1\] : reversed string
  * enumerate: index와 요소를 한 번에 리턴
  * int(x, base): x를 base진수로 변환

[divmod]: https://github.com/kim-ji-youn/tutorials/blob/main/Python/divmod.md
[int 함수]: https://github.com/kim-ji-youn/tutorials/blob/main/Python/int.md

#### 3. Str 다루기
##### 3-1. 문자열 정렬하기 : [ljust, center, rjust]
* ljust(width, \[filler\]): width 크기로 왼쪽 정렬
* center(width, \[filler\]): width 크기로 가운데 정렬
* rjust(width, \[filler\]): width 크기로 오른쪽 정렬

##### 3-2. 알파벳 출력하기 : [string 모듈]
* string 모듈
    * string.ascii_lowercase: 소문자 출력
    * string.ascii_uppercase: 대문자 출력
    * string.ascii_letters: 소문자와 대문자 출력
    * string.digits: 숫자 출력

[ljust, center, rjust]: https://github.com/kim-ji-youn/tutorials/blob/main/Python/rjust_center_ljust.md
[string 모듈]: https://github.com/kim-ji-youn/tutorials/blob/main/Python/string_module.md

#### 4. Iterable 다루기
##### 4-1. 원본을 유지한채, 정렬된 리스트 구하기 : [sorted]
* list1.sort() : list1의 순서가 바뀐다.  
* list2 = sorted(list1) : list1을 유지한 채, 정렬시키는 것이 가능하다. 

##### 4-2. 2차원 리스트 뒤집기 : [zip]




