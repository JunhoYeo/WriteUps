# NYPC 2018 - Day 1

## #3 아이템 구매
점수 : **100** / 100

백준 2839번 '설탕 배달' 문제와 유사하다. 구글링하면 알고리즘이 설명된 글들이 많은데, 한번씩 읽어보고 금방 풀었다.

## #4 승리팀 찾기
점수 : **100** / 100

아래 경우로 나눠서 생각하자.

- 아이템전 -> 무조건 **1등**이 승리
- 스피드전
    - 들어온 시간(등수 및 리타이어)에 따라 점수 부여 후 팀별 점수 계산
    - 점수가 높은 팀 승리, **단, 동점 시 1등 유저가 있는 팀이 승리**

처음에 문제를 꼼꼼히 안 읽어서 스피드전의 동점 처리를 못했었다. 다행히 늦지 않게 다시 수정해서 제출할 수 있었다.

## #5 줄임말
점수 : **100** / 100

파이썬 만세! 

- `''.join([])`으로 문자열 리스트를 문자열로 만들 수 있다(아래 예시).

```py
list = ['a', 'b', 'c']
print(''.join(list))
# abc
```

- 굳이 더 설명할 게 없다. 
다른 언어를 문제풀이 주 언어로 사용하다가 이 문제를 풀기 위해서 파이썬을 처음 이용해보는 사람이라도 기본적인 구글링만으로 충분히 해결할 수 있지 않았을까 하는 문제다.

## #6 우물왕 김배찌
점수 : **100** / 100

평균을 구하자.

## #7 최고의 동접 구간을 찾아라!
점수 : **50** / 100

시간초과 때문에 노가다를 엄청 했는데 결국 어찌어찌해서 50점이라도 땄다.

- `for` 문으로 시간을 초단위로(1440초) 구현해서 흐름에 따라서 로그인, 로그아웃, 현재 접속자 계산, 동접구간(시작/종료 시간) 저장 등을 실행했다.
- 로컬에서 테스트할 때는 `f-string`을 사용해서 format parsing/packing을 했는데, NYPC 채점 환경의 Python 버전이 3.5.2라서 작동하지 않았다. 그래서 대신 `''.format()`을 이용해서 제출했다(이렇게 제출 횟수가 하나 늘었다).
- 이것만 빼면 day-1에 공개된 문제는 모두 만점인데... 정말 아쉽다.

## #8 버튼 게임
점수 : **100** / 100

처음에는 부분 점수를 노리고 `X, Y <= 10`인 케이스를 모두 구해서 딕셔너리에 저장하고 조회하는 식으로 풀려고 재귀함수를 짰는데, (수많은 최적화를 거치니) 예상 외로 은근히 괜찮아서 50점을 얻었다(Python 코드가 timeout에 걸려서 C로 포팅해서 제출했던 것으로 기억하는데, 해당 C 코드를 실수로 덮어써 버려서 지금은 찾을 수 없다).

이는 나중에 non-recursive로 바꿔서 해결했다.