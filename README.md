# algorithm-study
prography 5th algorithm study 룰 정리 

## Rule  

##### 시간

- 강남역 매주 화요일 7시 
- 매주 스터디룸은 각 주 스터디 회고 담당이 예약한다.

##### 스터디 방식  

- github을 통해 코드 공유 / 피드백
- 프로그래머스 고득점 kit 10개 관련 개념 스터디 + 문제 풀이. 
- 10가지 개념은 프로그래머스에서, 문제는 leetcode 에서 뽑아 진행한다. 
  - 개념: https://programmers.co.kr/learn/challenges?tab=algorithm_practice_kit 
  - 문제:  https://leetcode.com 
- 매주 2개씩 스터디 총 5주를 진행한다.
- 모든 스터디 원들은 2가지 유형에 대한 개념 공부와 그에 해당하는 알고리즘 문제 풀기
- 문제는 유형별 2문제
  - 스택/큐 경우 두가지 유형이기 때문에 4문제를 풀어야함 
- 각 유형별로 한명씩 맡아 개념을 정리해오고, 관련 개념을 설명한다. 
- 이후 해당 개념에 대해 풀어온 코드들을 리뷰한다. 
- 해당 코드 리뷰어는 랜덤으로 뽑고, 설명을 하지 못했을 경우 과제 미비로 벌금을 내야한다
- 매주 1명이 맡아 스터디 관련 내용을 기록한다 
  - 새로 알게 된 내용, 몰라서 찾아본 내용, 벌금 관련 정리 등
  - Readme.md 에 매주 정리해서 올려놓는다 

##### 알고리즘 문제 제출 관련 

- 모든 스터디원들은, 스터디 전날 22:00 까지 자신의 푼 코드를 github 에 올린다 
- 문제는  https://leetcode.com 에서 선별하며, 풀 문제는 관련 발표자가 제공한다.
  - 문제가 어렵더라도 leetcode 에 답 보고 공부해오기! 
- 파일 형식은  문제이름_자기이름.py (다 소문자)
- 첫주는 .md 파일로 정리해서 한 파일에 코드 붙혀넣어 올리기! 
- 문제 속도 주석으로 달아놓기!! 

##### 발표 관련

- 발표자료는 .md 파일의 형식을 가진다.
- 알고리즘 기술 면접때 대답할 수 있을 정도의 간단한 자료면 충분하다.
- 발표 자료는 월요일까지 안올려도됨. 



##### ⭐️ 벌금 관련 ⭐️

##### 지각

- 첫 지각은 1,000 원부터
- 이후 피보나치 수열로 오른다
  - 1, 1, 2, 3, 5, ...

##### 결석

- 1번 결석 면제, 이후 5,000원 

##### 과제 안할 경우 

- 월요일 22:00 시 미제출 경우 
  - 1,000원 + 피보나치 (지각 동일)
- 화요일에 랜덤으로 정해서 코드 리뷰를 한다.  설명 못하면 과제 1000원! 

##### 기타

- 해당 5주가 끝난 이후 코딩 테스트 문제 풀어보기 
- 매주 스터디 끝나고 방식 논의하면서 차츰 수정하기 
- 예지 자료구조 A+ 기원



## 회고

10/29

##### is 연산자

'is' 연산자는 포인터(레퍼런스)를 비교하는 연산자이지, 데이터를 비교하는 연산자가 아니라는 점을 설명할 수 있다. 'is' 커맨드는 가급적이면 상수(None, True, False 등)를 비교하는데만 쓰도록 하자. 예를 들자면 varA is not None 이런 식으로...
<http://seorenn.blogspot.com/2011/04/python-is.html>



##### ^ - XOR 비트 상호배제 

> 비트 상호배제는 같은 자리의 값이 서로 다르면 해당 자리의 연산 결과가 1이며 같을 때 0입니다. 예를 들어 a가 6이고 b가 3일 때 a^b는 5입니다.(110^011 => 101) 

```python
    def singleNumber(self, nums: List[int]) -> int:
        answer = 0
        for elem in nums:
            answer = answer ^ elem
```



##### 자료를 소팅된 상태로 저장해야 한다면 무슨 자료 구조를 써야 할까요?

트리를 사용할 것 같다. in order traversal 방식을 사용하면 자동으로 소팅이 되어있다. 

or

AVL 트리는 모든 internal node v에 대해, v의 자식들의 높이가 최대 1만큼만 차이가 나는 이진 탐색 트리이다. insert나 remove할 때 높이차가 2이상이면, 데이터를 재구조화하기 때문에 유용할 것 같다! 

(p.s 면접 담당자가 좋아함)





## 2019/10/15

1주차 - 슈퍼스타트 강남점 7시 

- 동적 계획법 
  - 발표 : 이동주
  - 문제 
    - https://leetcode.com/problems/maximum-subarray/
    - https://leetcode.com/problems/climbing-stairs/
- 스택 / 큐
  - 발표 : 장지창

    - https://planjang.tistory.com/211
  - 문제

    <스택>

    - https://leetcode.com/problems/valid-parentheses/

    - https://leetcode.com/problems/min-stack/

      <큐>

    - https://leetcode.com/problems/number-of-recent-calls/

    - https://programmers.co.kr/learn/courses/30/lessons/42587

- 회고: 한수민

  - 스터디 브랜치는 자신의 영어 이름으로 판다.

  - __src/name__  안에 _week.md_  로 파기

  - 문제 제목은 h1 로 , 안의 내용은 "```python" 으로 명시하기 

  - 시간복잡도 넣기 

  - ```python
    def is_parentheses_match(expr):
    	lefty = "({["
    	righty = ")}]"
    	S = ArrayStack()
    for x in expr:
       if c in lefty:
       	  S.push(c)
       elif c in righty:
       if S.is_empty():
           return False
       if righty.index(c) != lefty.index(S.pop()):
           return False
    return S.is_empty()
    ```



## 2019/10/29

2주차 - 스터디 블룸 7시 

- 트리

  - 발표: 조예지
    - <https://leetcode.com/problems/maximum-depth-of-binary-tree/>
    - <https://leetcode.com/problems/merge-two-binary-trees/>

- 해시
  - 발표: 한수민

  - 문제

    - <https://leetcode.com/problems/single-number/>
    - <https://leetcode.com/problems/two-sum/>

##### 지각

- 지각 : 이동주 (1,000원)
- 결석 : 김은향 (1번 면제)
- 과제 : 김은향 (1,000원)



## 2019/11/05

- 정렬
  - 발표: 김건호
  - 문제
    - <https://leetcode.com/problems/k-closest-points-to-origin/>
    - <https://leetcode.com/problems/valid-anagram/>

- 힙
  - 발표: 김은향
  - 문제 
    - <https://leetcode.com/problems/last-stone-weight/>
    - <https://leetcode.com/problems/top-k-frequent-elements/>
