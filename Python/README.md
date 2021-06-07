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
Iterable : 자신의 멤버를 한번에 리턴할 수 있는 객체    
ex) list, str, tuple, dictionary 등
##### 4-1. 원본을 유지한채, 정렬된 리스트 구하기 : [sorted]
* list1.sort() : list1의 원소를 정렬
* list2 = sorted(list1) : list1을 유지한 채, 다른 변수에 정렬된 리스트를 저장

[sorted]: https://github.com/kim-ji-youn/tutorials/blob/main/Python/sorted.md

##### 4-2. 2차원 리스트 뒤집기 : [zip]
##### 4-3. i번째 원소와 i+1번째 원소 : [zip]
##### 4-4. 모든 멤버의 type 변환하기 : [map]


[zip]:https://github.com/kim-ji-youn/tutorials/blob/main/Python/zip.md
[map]:https://github.com/kim-ji-youn/tutorials/blob/main/Python/map.md

#### 5. Sequence Types 다루기
Sequence Type: int 타입 인덱스를 통해 원소를 접근할 수 있는 iterable    
ex) list, str, tuple
##### 5-1. sequence 멤버를 하나로 이어붙이기: [join]
##### 5-2. sequence type의 * 연산 : \*

[join]:https://github.com/kim-ji-youn/tutorials/blob/main/Python/join.md

#### 6. Itertools/Collections 모듈
##### 6-1. 곱집합(Cartesian product) 구하기: [product]
* itertools.product : 곱집합을 구해준다. 
##### 6-2. 2차원 리스트를 1차원 리스트로 만들기: [from_iterable]

[product]: https://github.com/kim-ji-youn/tutorials/blob/main/Python/product.md
[from_iterable]: https://github.com/kim-ji-youn/tutorials/blob/main/Python/from_iterable.md


