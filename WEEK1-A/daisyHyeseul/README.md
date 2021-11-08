# WEEK1 \_ 다양한 자료 구조

## 리스트

## 스택

```cpp
	stack<int> s;
```

## 큐

## 우선순위큐

## > 힙 (heap)

최댓값 및 최솟값을 찾아내는 연산을 빠르게 하기 위해 고안된 완전이진트리(complete binary tree)를 기본으로 한 자료구조(tree-based structure)

**" A가 B의 부모노드(parent node) 이면, A의 키(key)값과 B의 키값 사이에는 대소관계가 성립한다. "**

- 최소힙
  : 부모노드의 키값이 자식노드의 키 값보다 항상 작은 힙

- 최대힙 : 부모노드의 키값이 자식노드의 키값보다 항상 큰 힙
- 힙에서는 가장 높거나 낮은 우선순위를 가지는 노드가 항상 root node에 오기 때문에, **우선순위 큐**와 같은 자료형을 구현하는데 사용할 수 있다.

"부모노드와 자식노드 간에만 대소관계가 있으며, **형제 간에는 대소 관계가 정해져 있지 않다**"

- 시간 복잡도 : O(log n)

## > 구현

### 1. **priority queue**

- c++에서 제공하는 기본적인 우선순위 큐
  > 기본 형태 :
  ```cpp
  priority_queue<a,vector\<a>,greater\<a>>
  (최소힙 구현 시)
  ```

````

> 만약 우선순위를 지정해주고 싶다면 greater자리에 직접 compare 구조체를 만들어서 대입해주면 된다.

```cpp
struct cmp{
    bool operator()(a t, a u){
        return t.value < u.value;
    }
};
```

### 2. 배열로 구현

- 현재 노드가 n 일 때 부모노드는 n/2, 자식노드는 n\*2 또는 n\*2 + 1 로 접근한다.
- 삽입 : 이진트리 가장 끝에 원소를 추가하고, 추가한 부분의 원소와 해당 원소의 부모 노드와 크기를 비교하고 바꿔가면서 위치를 찾아간다.
- 삭제 : 힙의 가장 첫번째 원소를 반환하고 첫번째 위치에 힙의 가장 끝 원소를 대입한다. 그리고 힙 재정렬!
````