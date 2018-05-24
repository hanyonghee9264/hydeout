---
layout: post
title: 흐름제어(if,for,while)
excerpt_separator:  <!--more-->
---

### 소수판별문제

- 1 ~ 1000까지 숫자중에 소수만 출력
TIP. 소수는 1과 자기자신으로만 나누어 떨어지는 숫자

```python
for i in range(1, 1001):      # 1부터 1000까지 숫자 순회
    key = True                # for문을 하나 더 이용해서
    for j in range(2,i):      # i보다 작은 2부터 'i'전 까지
        if i % j == 0:        # 그 어떤 숫자중에 i를 나눠 떨어지게 한다면
            key = False       # 그 값은 False
            break             # 브레이크를 만나서 끝나든 그렇지 않든
    if key:                   # 이 부분이 실행이 됨 (바깥의 for문이기 때문에 새로운 for문을 돌기전에 항상 이 부분이 실행 됨)
        print(i)
```
> 키 값이 True면 그 밑에 for문 부터 계속 실행 되지만 만약에 i가 j로 나누어 떨어졌을 때 0이면, 소수가 아니게 된다. 그래서 break가 걸리지만
밑에 있는 if key 값은 바깥의 for문이기 때문에 항상 실행됨 (1~ 1000까지)
