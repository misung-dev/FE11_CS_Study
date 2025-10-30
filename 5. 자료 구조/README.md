# 🏗️ 자료구조

## 5.1 복잡도

### 5.1.1 시간 복잡도

- 시간 복잡도? 입력 크기에 대해 어떠한 알고리즘이 실행되는데 걸리는 시간

  - 예시

    1. 첫 번째 반복문의 시간 복잡도는 O(10\*n^2) = O(n^2) 이다.
    2. 두 번째 반복문의 시간 복잡도는 O(n) 이다.
    3. 해당 알고리즘의 시간 복잡도는 O(n^2) + O(n) = O(n^2) 이다.

    ````
    for (int i = 0; i < 10; i++) {
    for (int j = 0; j < n; j++) {
    for (int k = 0; k < n; k++) {
    if (true) System.out.println(k);
    }
    }
    }

        for (int i = 0; i < n; i++) {
            if (true) System.out.println(i);
        }
        ```
    ````

- 빅오 표기법? 알고리즘의 효율성을 표기해주는 표기법

- 시간 복잡도 존재의 이유

  - 효율적인 코드로 개선하는 데 쓰이는 척도
  - O(n^2)보다는 O(n), O(n)보다는 O(1)을 지향

    <img height=200 src='https://velog.velcdn.com/images/dbfla0628/post/0aa6133d-f488-4cfd-bd0e-de58eff2df3c/image.png'>

### 5.1.2 공간 복잡도

- 공간 복잡도? 프로그램을 실행시켰을 때 필요로 하는 자원 공간의 양

### 5.1.3 자료 구조에서의 시간 복잡도

  <img height=400 src='https://velog.velcdn.com/images/no88888888/post/dcd02d6b-e34d-4bf2-9c58-3f5fd381c50f/image.png'>

## (추가) 자료 구조 큰 그림 👀

  <img height=300 src='https://images.velog.io/images/y1andyu/post/f226dfb0-0ff2-40a3-839b-2138899e9ba3/%EC%9E%90%EB%A3%8C%EA%B5%AC%EC%A1%B0%EC%9D%98-%EC%A0%84%EC%B2%B4-%EB%B6%84%EB%A5%98.png'>

## 5.2 선형 자료 구조

- 선형 자료 구조? 요소가 일렬로 나열되어 있는 자료 구조

  <img height=300 src='https://velog.velcdn.com/images/hxezu/post/8546cb4f-c98e-40db-b9ff-62294671b375/image.png'>

### 5.2.1 연결리스트

- 연결 리스트? 데이터를 감싼 노드를 포인터로 연결해서 공간적인 효율성을 극대화시킨 자료 구조

  - 싱글 연결 리스트: next 포인터만을 가지면서 현 노드에서 다음 노드만을 가리키는 형태
  - 이중 연결 리스트: next 포인터와 prev포인터 두개를 가진 형태를 말하며 next 포인터는 다음 노드, prev 포인터는 이전 노드를 가리키는 형태
  - 원형 연결 리스트: 이중 연결 리스트와 유사하지만 마지막 노드의 next 포인터가 헤드 노드를 가리키는 것

    <img height=200 src='https://velog.velcdn.com/images/sean2337/post/e70d5fbf-db4a-4158-98fe-bb82f916d71b/image.png'>

### 5.2.2 배열

- 특징

  - 같은 타입의 변수로 구성
  - 크기가 정해져 있고인접한 메모리 위치에 있는 데이터를 모아놓은 집합
  - 중복 허용 및 순서 존재

- 랜덤 접근(=직접 접근): 임의의 인덱스에 해당하는 데이터에 접근
- 순차적 접근: 저장된 순서대로 검색해야 하는 접근법

  <img height=200 src='https://velog.velcdn.com/images/sean2337/post/b26c4dc7-ef46-4184-9548-468ef3e2309b/image.png'>

- 배열과 연결리스트 비교

  <img height=300 src='https://velog.velcdn.com/images/dlgosla/post/d807e637-3d2d-47e0-b6ab-4308807daf4c/image.png'>

  <img height=200 src='https://blog.kakaocdn.net/dna/cLMZMC/btr7eWXfals/AAAAAAAAAAAAAAAAAAAAAJW_GNCCEXKm9LaY_hc7_CGzKEz1XUzQ8U4fyEvgroUh/img.png?credential=yqXZFxpELC7KVnFOS48ylbz2pIh7yKj8&expires=1761922799&allow_ip=&allow_referer=&signature=NWhyC36tUlKE%2FqEpN%2B3%2Fer7RbjY%3D'>

### 5.2.3 벡터

- 동적 할당되는 배열.
- 메모리 heap에 생성되며 각 원소의 메모리 주소가 연속적
- 임의 원소 접근이 빠르지만, 중간 삽입 삭제 시 메모리의 재할당 및 복사가 발생하므로 느림

  <img height=150 src='https://velog.velcdn.com/images/woojoo0407/post/9b14b4c9-b268-49a7-a370-3cea82e44b6f/image.png'>

### 5.2.4 스택

- 스택은 가장 마지막에 들어간 데이터가 가장 먼저 나오는 LIFO(Last In First Out) 성질을 가진 자료구조
- 재귀적인 함수, 알고리즘, 웹 브라우저 방문 기록 등에 쓰인다.
- 삽입과 삭제에 O(1), 탐색에 O(n)이 걸린다.

### 5.2.5 큐

- 큐는 먼저 집어넣은 데이터가 먼저 나오는 FIFO(First In First Out) 성질을 가진 자료구조
- CPU 작업을 기다리는 프로세스, 스레드 행렬 또는 네트워크 접속을 기다리는 행렬, 너비 우선 탐색, 캐시 등에 사용된다.
- 삽입과 삭제에 O(1), 탐색에 O(n)이 걸린다.

## 5.3 비선형 자료 구조

### 5.3.1 그래프

- 그래프: 정점과 간선으로 이루어진 자료 구조

  - 정점(vertex) : 위치 (=node)
  - 간선(edge) : 위치 간의 관계, 즉, 노드를 연결하는 선
  - 예시

    - "어떠한 위치나 어떠한 사람"으로부터 "무언가를 통해 간다"라고 했을 때
    - "어떠한 위치나 어떠한 사람" 정점(Vertex)이 되고 "무언가를 통해 간다"는 간선(Edge)이 됩니다.

  <img height=200 src='https://postfiles.pstatic.net/MjAyMTEyMjhfODcg/MDAxNjQwNjQ2MzQzMzU5.BU8s-Mg7Y5pJCf1qA3Uko6RU4EWoPHjpbfrWOgWVsSog.ErUz1KQyUsFAjnSVShWQulfak99OqiGX4CrjqP9pXXYg.PNG.jhc9639/%EC%A7%91%ED%95%84%EA%B7%B8%EB%A6%BC.png?type=w966'>

- 단방향 간선
  <img height=200 src='https://postfiles.pstatic.net/MjAyMTEyMjhfMjc4/MDAxNjQwNjQ2NDczMTgz.i_2XWauD4ITXa7RxBZMMtumi41Nnuq_ncdgCDmgoZ2cg.qmiOBYBZmJAk4G-mI2arnWbRlPCnaxSRc77ITUbM5p8g.PNG.jhc9639/%EC%A7%91%ED%95%84%EA%B7%B8%EB%A6%BC.png?type=w966'>
- 양방향 간선
  <img height=200 src='https://postfiles.pstatic.net/MjAyMTEyMjhfMTQ5/MDAxNjQwNjQ2NjM0NDkz.83-TsLvCCZeqN2OXxJ556PNVP5e79Lwj9dzPt4S4cV4g.9oXrSI6NbBx_kndoArI6ypSvzOD5Dw_Mb_upbCxDkPwg.PNG.jhc9639/%EC%A7%91%ED%95%84%EA%B7%B8%EB%A6%BC.png?type=w966'>
- 그래프
  <img height=200 src='https://postfiles.pstatic.net/MjAyMjA0MTdfNjgg/MDAxNjUwMjA2NDIyMzE1.B-LRF9lTrj6t620TBwAZLDsjYqWS-w1y6YyDmE-3D_Mg.FuRTUeGih4OkMZkKV_uyC0xTxixJUCVBuAhzQ_sXOzgg.JPEG.jhc9639/12.JPG?type=w966' />

  <img height=200 src='https://laboputer.github.io/assets/img/algorithm/ds/06_graph2.PNG'>

- 가중치: 간선과 정점 사이에 드는 비용

  - 간선에 비용이나 가중치가 할당된 그래프
  - '네트워크' 라고도 한다.
  - 예시: 도시-도시의 연결, 도로의 길이, 회로 소자의 용량, 통신망의 사용료 등

### 5.3.2 트리

- 트리? 트리 구조로 배열된 일종의 계층적 데이터 집합

- 특징

  - 부모 자식 계층 구조를 갖는다.
  - V(노드 수) - 1 = E(간선 수)라는 특징이 있다.
  - 임의의 두 노드 사이의 경로는 반드시 존재한다.

- 개념

  - 루트노드: 가장 위에 있는 노드를 뜻합니다. 보통 트리문제가 나오고 트리를 탐색할 때 루트노드를 중심으로 탐색을 하면 문제가 쉽게 풀리는 경우가 많습니다.
  - 내부노드: 루트노드와 리프노드 사이에 있는 노드
  - 리프노드: 자식노드가 없는 노드

    <img height=200 src='https://velog.velcdn.com/images/pswo1021/post/951dcee3-6919-44e0-b3f0-b576d4e02a60/image.png'>

- 트리의 높이와 레벨
  <img height=200 src='https://velog.velcdn.com/images/ehddnr7355/post/bfb72d23-adca-40e4-8da1-732c041cbeb3/image.png'>

- 이진 트리: 각각의 노드의 자식노드 수가 2개 이하로 구성되어있는 트리
  <img height=200 src='https://postfiles.pstatic.net/MjAyMjA0MTdfMTQ0/MDAxNjUwMjA2NTMwNDQ5.n1Ogc_3ZpyPFu4MI4E4BKmuWVJZzEoyVOH6GxSpW8esg.8QQQcuLBpLhf8jBDbLhkChIDi3Ir6Qe5k7V-f-0-FyEg.JPEG.jhc9639/141.JPG?type=w966'>

- 이진 탐색 트리: 이진트리의 일종으로 노드의 오른쪽 하위 트리에는 "노드의 값보다 큰 값"이 있는 노드만 포함되고 왼쪽 하위트리에는 "노드의 값보다 작은값"이 들어있는 트리
  <img height=200 src='https://postfiles.pstatic.net/MjAyMTEyMzBfMjE0/MDAxNjQwODM5NjgyMjk4.9VypmsgdXDjKvXzY5y-U2KEqK17pA7EERLIM34ZnsfQg.F0sGXUDmo5sQndTOeIrX8pjBAEwP602nm73lSB3jD70g.PNG.jhc9639/SE-12ec1b03-fff7-4bfd-8172-e71a303dc4e6.png?type=w966'>

- AVL 트리

  - 균형 이진 탐색 트리(Self-balancing Binary Search Tree)의 일종으로,
  - 트리의 높이를 항상 일정하게 유지하여 탐색, 삽입, 삭제 연산에서 O(log n)의 성능을 보장하는 자료구조
  - 삽입이나 삭제가 발생할 때마다 트리의 균형을 유지하기 위해 회전(Rotation) 연산을 사용
  - 비균형 트리로 인한 성능 저하를 방지
    <img height=200 src='https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSL13G2C6iwCOipHDCvreEKipxwemjoKyuMbw&s'>

- 레드 블랙 트리

  - 특징
    - 레드-블랙 트리는 자가 균형 이진 탐색 트리이다.
    - 이진 탐색 트리는 균형이 안맞을 경우, 최악 시간 복잡도는 O(N) 이다.
    - 하지만, RB Tree는 삽입, 삭제 동안 트리의 모양이 균형 잡히도록 각 노드들은 Red 혹은 Black의 색상을 가지고 모든 경우에서 O(lonN)의 시간 복잡도를 보장받는다.
  - 조건 (5가지)
    - 모든 노드는 빨간색 혹은 검은색이어야 합니다.
    - 루트 노드는 검은색이다.
    - 모든 NIL은 검은색이다. (NIL : null leaf, 자료를 갖지 않고 트리의 끝을 나타내는 리프 노드)
    - 빨간색 노드의 자식은 반드시 검은색이다.
    - NIL에서 루트 노드까지 가는 경로에서 만나는 검은색 노드의 개수가 같다.

  <img height=200 src='https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2Fq1wQx%2FbtshRxzoSc3%2FAAAAAAAAAAAAAAAAAAAAANO27_C6AMFiD-CUrSUyexA4PSV_zvSy01VcTUZtpb9O%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3D%252FCCT439Nfo04MMRMQywOPigpSQ0%253D'>

### 5.3.3 힙

- 힙? 완전 이진 트리로, 최댓값 또는 최솟값을 빠르게 찾을 수 있는 자료 구조
- 최대힙: 부모 노드 값이 자식 노드의 값보다 크거나 같은 완전 이진 트리
- 최소힙: 부모 노드 값이 자식 노드의 값보다 작거나 같은 완전 이진 트리다

  <img height=200 src='https://blog.kakaocdn.net/dna/RTAS9/btqAt7REyPh/AAAAAAAAAAAAAAAAAAAAAOr1rfaVEigqd3UWKIsz2w0zi7pmlTdieO6UhT1tG2yV/img.png?credential=yqXZFxpELC7KVnFOS48ylbz2pIh7yKj8&expires=1761922799&allow_ip=&allow_referer=&signature=jjfbWgbbez%2FH%2B8We2hTEwuFGjKM%3D'>

- 최대힙의 삽입

  1. 힙에 새로운 요소가 들어오면, 일단 새로운 노드를 힙의 마지막 노드에 이어서 삽입한다.
  2. 새로운 노드를 부모 노드들과 교환해서 힙의 성질을 만족시킨다.

  <img height=400 src='https://velog.velcdn.com/post-images%2Fholicme7%2F80df2f10-20ae-11ea-98a2-7355d7fc70cd%2Fmaxheap-insertion.png'>

- 최대힙의 삭제

  1. 최대 힙에서의 최댓값은 루트 노드이므로 루트 노드가 삭제된다.
     최대 힙(max heap)에서 삭제 연산은 최댓값을 가진 요소를 삭제하는 것이다.
  2. 삭제된 루트 노드에는 힙의 마지막 노드를 가져온다.
  3. 힙을 재구성한다.

  <img height=400 src='https://velog.velcdn.com/post-images%2Fholicme7%2F6e807760-20af-11ea-b8a5-09eea756748a%2Fmaxheap-delete.png'>

### 5.3.4 우선순위 큐

- 우선순위큐는 선입선출의 구조를 가진 큐와 다르게, 가장 우선순위가 높은 데이터를 먼저 꺼내기 위해 고안된 자료구조입니다.
- 우선순위 큐를 구현하기 위해서 일반적으로 힙을 사용합니다. (배열, 연결리스트로도 구현 가능)

  <img height=200 src='https://blog.kakaocdn.net/dna/coHEBM/btsshtvomiO/AAAAAAAAAAAAAAAAAAAAAOMkN4XGcvY6yGviQOYMAYLl-ahH3PVr-Jfi1wtNARkJ/img.png?credential=yqXZFxpELC7KVnFOS48ylbz2pIh7yKj8&expires=1761922799&allow_ip=&allow_referer=&signature=3cYq20I%2FPjF2h7DYpqkmG4QtpNw%3D'>

### 5.3.5 맵

- 맵? 키-값 쌍(key-value pair)으로 데이터를 저장하는 추상적인 자료구조
- 특징:
  - 키(key)는 고유한 식별자 역할을 하며, 이를 통해 해당 값(value)에 접근 가능
- 장점
  - 중복된 키를 허용하지 않으며,
  - 키를 사용해 값을 빠르게 검색할 수 있다는 점입니다.
- 단점
  - 값은 중복될 수 있습니다.
- 종류: 해시맵(HashMap), 트리맵(TreeMap), LinkedHashMap 등

### 5.3.6 셋

- 셋 (=집합): 중복되지 않는 원소들의 모임으로 수학적인 집합 개념을 컴퓨터 과학의 문제에 적용하기 위해서 만들어진 자료구조
- 특징
  - 고유한 원소: Set은 각 원소가 중복되지 않는다. Unique한 원소.
  - 순서 없음: Set에서는 원소의 순서를 보장하지 않는다. 순서가 없다.
  - 집합 연산: Set은 원소들 간의 합집합, 교집합, 차집합 등과 같은 집합연산을 지원한다.

### 5.3.7 해시 테이블

- 해시맵과 해시테이블 무엇이 다른가?

  - 개념적으로는 같다 → 둘 다 “해시 기반의 키-값 저장소”.
  - 구현적으로는 다르다 → HashMap은 최신, 효율적이고 동기화되지 않음.
    Hashtable은 오래된 클래스이며, 기본적으로 동기화되어 있음.
    <img height=200 src='https://minho-jang.github.io/assets/images/dev/hash-1.png'>

## 스터디 끝~~

  <img height=200 src='https://cdn.ziksir.com/news/photo/201711/5208_16891.jpg'>
  <img height=200 src='https://i.pinimg.com/1200x/e8/e1/a9/e8e1a97b1af0b9636f40bf01ed44b917.jpg'>
