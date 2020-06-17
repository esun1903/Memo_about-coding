# Memo_about-coding

20-05-24

최근 풀어본 문제에서 내가 문제를 이해하고 구현하는 부분에서 자주 막히는 것을 알게됨!

막혔던 문제는 그래프에 관한 문제.

### 그래프
  - 트리보다 더 큰 의미임.
  - 단방향 그래프 , 양방향 그래프 2가지의 종류가 있다 
  - 그래프에는 가중치가 있을 수 있다.
  
### 트리 
   - 그래프보단 작은 범주에 속함 
   - 싸이클이 없어야됨 ex) 8번으로 시작해서 8로 돌아오면 안됨 (트리의 조건)
   
   
   ------------------------------------------------------------------------------
   
   #### 해결방법 ( 총 3가지 ) 
   
    1) Node 클래스 구현 ( 3가지 방법 중 가장 어려운 방법, 그리고 내가 문제에서 이렇게 풀려다가 시간이 다감 ) -> 트리 구현
    
    2) 2차원 배열 [][] , 가장 쉬운 방법 (거의 모든 문제를 풀 수 있는 방법)
   
    3) LinkedList (적은 확률이지만 풀 수 있는 방법이고 내가 푼 그래프에선 LinkedList로 푸는 게 더 효율적인 방법이었다. )  ,BFS and DFS 1260문제가 대표적.
                            
   
 ## Queue<int> queue = new LinkedList<>();
  
 Java에서는 Queue를 편리하게 사용할 수 있도록 API를 제공합니다.
 그리고 자바의 "다형성" 을 위해 ( 같은 자료형에 여러 가지 객체를 대입하여 다양한 결과를 얻어내는 성질을 의미)
 Java의 Queue는 인터페이스 형태이므로 inkedList 또는 ArrayList를 통해 사용할 수 있습니다.

 주요 메소드는 다음과 같습니다.
  
  Method                     Description 

Object element()	        저장된 요소를 읽어옴

 Object peek()	      큐의 맨 끝에 저장된 객체를 반환

 Object remove()	         큐에서 객체를 삭제

 boolean offer(Object o)	 큐에 객체를 저장


출처: https://swalloow.tistory.com/32 [MyCloud]


## Queue(큐) 개념
 큐는 스택과 마찬가지로 일종의 리스트
 데이터 삽입은 한쪽 끝에서, 삭제는 반대쪽 끝에서만 일어난다
 삽입이 일어나는 쪽을 rear, 삭제가 일어나는 쪽을 front라고 부른다.
 
 FIFO(First-in, First-Out)


 Queue(큐)에서 지원하는 연산
insert, enqueue, offer, push : queue의 rear에 새로운 원소를 삽입하는 연산

remove, dequeue, poll, pop : queue의 front에 있는 원소를 queue로부터 삭제하고 반환하는 연산

peek, element, front : 큐의 front에 있는 원소를 제거하지 않고 반환하는 연산

is_empty : 큐가 비었는지 검사

Queue(큐)의 응용
cpu 스케쥴링 : multitasking 환경에서 프로세스들은 큐에서 cpu가 할당되기를 기다린다.

데이터 버퍼 : 네트워크를 통해 전송되는 패킷들은 도착한 순서대로 버퍼에 저장되어 처리되기를 기다린다

자원을 공유하는 대부분의 경우에 큐가 사용 된다
