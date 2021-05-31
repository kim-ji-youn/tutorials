**[Pragrammers]의 [파이썬을 파이썬답게] 수업을 정리한 것입니다.**

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


#### 2. 정수
##### 2-1. 몫과 나머지: divmod
```
>>> divmod(x, y)
```
argument: x = 실수, y = 실수
return value: (몫, 나머지)

예시 1 - 양의 정수
```
>>> divmod(4, 2)
(2, 0)
>>> divmod(8, 3)
(2, 2)
```

예시 2 - 음의 정수
```
>>>divmod(12, -5)
(-3, -3)
>>>divmod(-12, 5)
(-3, 3)
>>>divmod(-12, -5)
(2, -2)
```

예시 3 - 실수
```
>>>divmod(3.6, 2)
(1.0, 1.6)
>>>divmod(3.6, 0.5)
(7.0, 0.10000000000000009)
>>>divmod(4, 0.3)
(13.0, 0.10000000000000014)
```

divmod(a, b)의 값을 unpacking 하여 print
```
print(*divmod(a, b)) 
```
--> 몫과 나머지가 띄어쓰기로 구분되어 print


