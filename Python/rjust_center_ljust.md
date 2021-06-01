#### 3. Str 다루기
##### 3-1. 문자열 정렬하기

* **문제**: 문자열 s를 좌측, 가운데, 우측 정렬한 길이 n인 문자열을 프린트
내가 작성한 코드는 아래와 같다. 
```
s, n = input().strip().split(' ')
n = int(n)
print(s)
print(' '* int((n-len(s))//2) + s)
print(' '* (n-len(s)) + s)
```

강의에 등장한 파이썬스럽지 않은 코드 예시는 for문을 사용한다. 
```
s, n = input().strip().split(' ')
answer = ''
for i in range(n-len(s)) :
  answer += ' '
answer += s
```

파이썬다운 코드는 아래와 같다. 
```
s, n = input().strip().split(' ')
n = int(n)

s.ljust(n) #좌측 정렬
s.center(n) #가운데 정렬
s.rjust(n) #우측 정렬
```

* **요약**
* 좌측, 가운데, 우측 정렬은 for문 사용하지 말고 아래 함수를 쓰자!
    * string.ljust(n, f) : 길이 n만큼 좌측 정렬, f는 filler(optional)
    * string.center(n, f) :  길이 n만큼 가운데 정렬, f는 filler(optional)
    * string.rjust(n, f): 길이 n만큼 우측 정렬, f는 filler(optional)
