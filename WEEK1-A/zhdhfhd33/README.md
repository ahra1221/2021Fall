## heap<br>
정렬된 상황을 유지해야하는 상황에서 리스트, 배열은 삽입 삭제가 O(N)이 걸리므로 log N이 걸리는 heap을 사용하는 것을 고려할만 하다.<br>
다만 heap구현 시 upheap(push), downheap(pop)의 과정이 구현하기 쉽지는 않은 듯. STL priority queue가 있다고 하니 알아보자.<br>

## boj1655
처음에 떠오른 것은 AVL tree였다. 열심히 만들던 중 알고보니 커리큘럼에 AVL tree가 없었다. 그래서 포기. 많은 공부가 되었다.<br>
그 다음 떠오른 것은 배열. 빈 배열 부터 시작해서 채워나가면 n^2에 구현이 가능했다. 근데 입력 개수의 최대가 10만개. 제곱하면 어림잡아 연산횟수가 100억이었다. 1억 당 1초로 어림계산한다고 했을 때 100초가 예상됨. 포기.<br>
이 정도로 시간복잡도가 주어진다면 heap을 사용해야하는 듯 했다. 여기저기 아이디어를 조금씩 주워서 성공했다.<br>

## boj3015
모르겠다. 직관적으로 와닿지가 않는다. 시간을 두고 많이 봐야할듯.

## boj11003
큐와 pair를 사용해야된다고 생각했었으나 deque와 pair를 사용해야 가능한 문제였다.
큐, 스택으로 n^2걸리는 알고리즘을 개선하는 것을 보고 queue, stack들에 대해서 많이 공부해야할 듯.

이것을 슬라이딩 윈도우 알고리즘이라고 한다.



