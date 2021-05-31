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
