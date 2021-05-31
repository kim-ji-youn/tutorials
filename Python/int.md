#### 2. 정수 다루기
##### 2-2. n진법 -> 10진법: int 함수
나는 이렇게 짰다
```
num, base = map(int, input().strip().split()

answer = 0
i = 0
while num > 0 :
  answer += (num%10) * (base**i)
  num = num // 10
  i += 1
print(answer)
```

이것은 파이썬답지 않은 코드..
```
num = '3212'
base = 5

answer = 0
for idx, number in enumerate(num[::-1]) :
  answer += int(number) * (base ** idx)
```
* enumerate
* num\[::-1\]

파이썬다운 코드
```
num = '3212'
base = 5
answer = int(num, base)
```
* int(x, base) : base 진법으로 변환
    * argument: x = string 타입, base = 진수
    * return value : x를 base 진수로 바꾼 것, 기본은 10진수

