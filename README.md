# algorithm-study

프로그라피 5기 알고리즘 스터디 입니다.

4주간 프로그래머스 단계별 알고리즘 문제 스터디 진행방식 및 회고입니다.

## Rule  

#### ⏱ 시간

- 역삼역 매주 토요일 11시 (4주)
- 매주 스터디룸은 각 주 스터디 회고 담당이 예약한다.
- 문제 제출 기한은 금요일 12시

#### ✏️ 스터디 방식  

- github을 통해 코드 공유 / 피드백

- 프로그래머스 단계별 문제 풀이

- ##### 코드 리뷰는 질문과 답변 성실하게, 온라인에서만 진행한다.

- 1주차 (LV1) 7문제, 

- 2주차 (LV2) 5문제,

- 3주차 (LV3)  3문제

- 4주차 (LV4,5) 2문제로 진행한다.

- __공통문제, 개별문제(1)문제__ 를 풀어오고, 개별 문제는 어떻게 접근했는지 자세히 서술한다

  example

  ```
  완주하지 못한 선수에서 해시를 썻다
  해시를 쓰면 문자열을 더욱 빠르게 찾기 웅앵웅
  시간 복잡도 ㅇㅇㅇ
  공간 복잡도 ㅇㅇㅇ
  이런식으로 접근해서 풀었다 
  ```

- 시간복잡도 공간 복잡도는 주석으로 작성해서 넣는다. 

- - 

- ##### 새로 안 사실 정해주기 

  ```
  파이썬 안 자료형의 구현
  이게 왜 재밌을까 생각해보면 씨나 자바 같은 언어는 인트가 사이즈가 있는데
  우리 항상 파이썬 인트 쓰면서 물어보지 않은 질문들?
  그런 작지만 은근 중요한 부분
  엄청 어렵지 않고 우리가 다 알아들을 수 있으나 모를 법한 것들
  그런거 하나씩 번갈아가면서 준비하는게 좋을거 같아
  ```

- ##### 코드를 짜면서 새로 배운 라이브러리가 있다면 공유하쟈 

- 





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



##### 자료를 소팅된 상태로 저장해야 한다면 무슨 자료 구조를 써야 할까요? (p.s 면접 담당자가 좋아함)

트리를 사용할 것 같다. in order traversal 방식을 사용하면 자동으로 소팅이 되어있다. 

or

AVL 트리는 모든 internal node v에 대해, v의 자식들의 높이가 최대 1만큼만 차이가 나는 이진 탐색 트리이다. insert나 remove할 때 높이차가 2이상이면, 데이터를 재구조화하기 때문에 유용할 것 같다! 



11/05

##### for _ in range(k)

인덱스 안쓸때 이런식으로 쓸 수 있다.

##### sort 와 sorted의 차이

- __sort()__
  원본을 직접 정렬 , None을 반환함

```python
list.sort()
```

- __sorted(list)__
  원본에 영향을 끼치지 않음, 정렬한 새로운 문자열 혹은 list를 반환함

##### collections.Counter()

컨테이너에 동일한 값의 자료가 몇개인지를 파악하는데 사용하는 객체이다.

- most_common(n)
  입력된 값의 요소들 중 빈도수(frequency)가 높은 순으로 상위 n개를 리스트(list) 안의 투플(tuple) 형태로 반환한다. n을 입력하지 않은 경우, 요소 전체를 [(‘값’, 개수)]의 형태로 반환한다.

```python
import collections

c2 = collections.Counter(‘apple, orange, grape’)
print(c2.most_common())
print(c2.most_common(3))
```

##### try-execept 차이

<https://excelsior-cjh.tistory.com/94> [EXCELSIOR]

- 효율적 측면
  - 99% try문을 통과할시 try, excepy를 쓰는게 낫고 50%이상이 try문을 통과하지 못할시 if else를 쓰는게 효율적
- 그 외 참고할 자료:  `None` 보다 예외를 발생시키자 (Effective Python: Better way 14)
  - `None`을 반환하는 함수는 후에 호출할 때 해당 값이 `None`인지 평가해줘야함 ( `if return_none_or_value() == None else…`)
  - 코드를 읽는 사람이 왜 `None`을 반환하는지 명확하게 유추할 수 없음 -> `raise CustomException`을 발생시켜서 명확히 어떤 상황인지 명시하는게 



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

##### 벌금

- 지각 : 이동주 (1,000원)
- 결석 : 김은향 (1번 면제)
- 과제 : 김은향 (1,000원)



## 2019/11/05

3주차 - 슈퍼스타트 7시 

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

##### 벌금

- 결석 : 장지창 (1번 면제) 🎂축생일🎂



## 2019/11/12

4주차 - 슈퍼스타트 7시

- 이분탐색
  - 발표: 장지창
  - 문제
    - <https://leetcode.com/problems/intersection-of-two-arrays-ii/>
    - <https://leetcode.com/problems/find-the-duplicate-number/>
- 그리디
  - 발표:손주영
  - 문제
    - <https://leetcode.com/problems/score-after-flipping-matrix/>
    - <https://leetcode.com/problems/minimum-add-to-make-parentheses-valid/>

##### 비고

- 결석으로 발표를 하지 못하는 코딩고수씨를 대신해, 깜짝손님 주영언니가 그리디를 발표하게 되었습니다!

##### 벌금

- 결석: 이동주 (1번 면제) 🎂축생일🎂
- 결석: 조예지 (1번 면제) 

- 과제 지각 : 조예지(1,000원), 김은향(1,000원)



## 2019/11/19

5주차 - 슈퍼스타트 7시 (예약자: 장고장)

- 그래프
  - 발표: 조예지
  - 문제
    - <https://leetcode.com/problems/find-the-town-judge/>
    - <https://leetcode.com/problems/regions-cut-by-slashes/>
- 완전탐색
  - 발표: 한수민 (발표할게 별로 없을것 같아, 문제 4개 + )
  - 문제: 프로그래머스 4문제
    - <https://programmers.co.kr/learn/courses/30/lessons/42840>
    - <https://programmers.co.kr/learn/courses/30/lessons/42839>
    - <https://programmers.co.kr/learn/courses/30/lessons/42841>
    - <https://programmers.co.kr/learn/courses/30/lessons/42842>

##### 벌금

- 과제 : 김은향 (2,000원), 장지창(1,000원), 이동주(1,000원), 조예지(1,000원), 한수민(1,000원)
- 결석 : 김건호 (1번 면제)

## 2019/11/26

6주차 

- ##### BFS

  - 발표: 김은향 
  - 문제:
    - https://leetcode.com/problems/maximum-depth-of-n-ary-tree/
    - https://leetcode.com/problems/binary-tree-level-order-traversal/submissions/

- ##### DFS

  - 발표: 김건호 
  - 문제
    - <https://leetcode.com/problems/symmetric-tree/>
    - <https://leetcode.com/problems/course-schedule/>

- 결석: 한수민 (1번 면제), 이동주(5,000원), 장지창(5,000원)

- 과제: 한수민 (2,000원), 장지창(1,000원), 김은향(3,000원)



## 2020/01/18 

- 1/18일 1주차 : 공통 6문제 + 개인문제 1문제 

- __업로드 폴더__ : __src/programmers__ 

- ##### 파일 명: __week1.md__ 

- ##### 공통문제

  - 모의고사 : <https://programmers.co.kr/learn/courses/30/lessons/42840>
  - 완주하지 못한 선수: <https://programmers.co.kr/learn/courses/30/lessons/42576>
  - 자릿 수 더하기: <https://programmers.co.kr/learn/courses/30/lessons/12931>
  - 예산: <https://programmers.co.kr/learn/courses/30/lessons/12982>
  - 실패율: <https://programmers.co.kr/learn/courses/30/lessons/42889>
  - 다트게임: <https://programmers.co.kr/learn/courses/30/lessons/17682>

- ##### 개별문제

  - 이동주 
    - 하샤드 수 
    -  <https://programmers.co.kr/learn/courses/30/lessons/12947>
  - 장지창 
    - 행렬의 덧셈
    - <https://programmers.co.kr/learn/courses/30/lessons/12950>
  - 한수민 
    - 이상한 문자 만들기
    - <https://programmers.co.kr/learn/courses/30/lessons/12930>

- 비고 
  - 결석: 수민