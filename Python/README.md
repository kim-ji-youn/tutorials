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
##### 2-2. n진법 -> 10진법: [int]
  * string\[::-1\] : reversed string
  * enumerate: index와 요소를 한 번에 리턴
  * int(x, base): x를 base진수로 변환

[divmod]: https://github.com/kim-ji-youn/tutorials/blob/main/Python/divmod.md
[int]: https://github.com/kim-ji-youn/tutorials/blob/main/Python/int.md

#### 3. Str 다루기
##### 3-1. 문자열 정렬하기 : [ljust, center, rjust]
* ljust(width, \[filler\]): width 크기로 왼쪽 정렬
* center(width, \[filler\]): width 크기로 가운데 정렬
* rjust(width, \[filler\]): width 크기로 오른쪽 정렬

##### 3-2. 알파벳 출력하기 : [import string]
* string 모듈
    * string.ascii_lowercase: 소문자 출력
    * string.ascii_uppercase: 대문자 출력
    * string.ascii_letters: 소문자와 대문자 출력
    * string.digits: 숫자 출력


[ljust, center, rjust]: https://github.com/kim-ji-youn/tutorials/blob/main/Python/rjust_center_ljust.md
[import string]: 

