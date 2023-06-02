### chap12
***

### 컬렉션 프레임워크
- Collection Framework는 크게 3가지 인터페이스중 한 가지를 상속받아 구현해 놓앗다.
- 1. list 인터페이스
- 2. set 인터페이스
- 3. map 인터페이스

- list 인터페이스와 set 인터페이스의 공통부분을 collection 인터페이스에서 정의 하고있다
- 하지만 map은 구조상의 차이로 collection 인터페이스에서 정의하고 있지 않다.

### 각 인터페이스 별 특징
*** 

#### List 인터페이스
- 순서가 있다, 중복저장이 허용된다
- vectior, arrayList,LinkedList,Stack,Queue등이 있다.

#### Set 인터페이스
- 순서가 없다, 중복저장이 허용되지 않는다
- HashSet,TreeSet 등이 있다

#### Map 인터페이스
- 키와 값이라는 한 쌍으로 이루어져있다
- key를 set방식으로 관리하기때문에 순서도없고 중복된 key는 안된다
- 값은 중복이 허용된다
- HashMap,TreeMap,HashTable,Poroperties 등이 있다.
***
### 설명
*** 
- List와 Set의 공통인 Collection 인터페이스 주요 메소드
- add(),clear(),contains(),equals(),isEmpty(),
- iterator(),remove(),toArray()등이 있다
***

### List 계열의 컬렉션
***
#### ArrayList
- 가장 많이 사용되는 컬렉션 클래스이다
- 인덱스를 이용해 배열요소에 빠르게 접근할 수있다
- 배열의 단점을 보안하기 위해 만들어졌다
- 배열의 크기는 변경불가하고 요소의 추가,삭제,정렬 기능들을 미리만든 메소드로 구현해서 편리하다
- 편리한것이지 속도가 빨라지는 것은 아니다
- array의 크게는 size()로 확인할 수있다 , 해당 인덱스 값을 가져올떄는 get()을 사용한다
-   ```
     System.out.println("alist의 size : " + alist.size());
    System.out.println(i + " : " + alist.get(i));
     ```
#### Iterator
- Collection 인터페이스의 interator() 메소드를 이용해서 인스턴스를 생성 할 수있다.
- 반복자라고 불리우며 반복문을 이용해서 목록을 하나씩 꺼내는 방식으로 사용하기 위함이다
- 인덱스로 관리되는 컬렉션이 아닌경우 반복문을 사용해서 요소를 하나씩 접근할 수 없기 때문에
- 인덱스를 사용하지않고 목록을 만들어 주는 역할이라고 보면된다.
- hasNext(): 다음요소를 가지고있는경우 true, 뒤에 더이상 요소가 없으면 fasle를 반환함
- next():다음요소를 반환

#### AscendingPrice
- 숫자배열을 오름차순으로 정렬하고,중복되는 숫자는 없는것으로간주함
- 