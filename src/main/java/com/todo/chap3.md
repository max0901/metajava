### chap3
***

### 메소드란
- 어떤 특정 작업을 수행하기 위한 명령문의 집합이라고 할 수 있다

### 변수의 종류
- 지역변수 : 선언한 메소드 블럭 내부에서만 사용이 가능하다. 이것을 지역변수의 스코프라고 한다
- 매개변수 : 메소드 선언부 괄호 안에 전달 인자를 받기위해 선언하는 변수를 매개 변수라고 한다 
- 전역 변수(필드) : 
- 클래스(static) 변수

### return
 return은 현재 메소드를 강제 종료하고 호출한 구문으로 다시 돌아가는 명령어이다.
 
### static메소드인경우
- 다른 클래스에 작성한 static 메소드의 경우 호출할 때 클래스명을 반드시 기술해야 한다.
- 클래스명.메소드명()

### 패키지
- 서로 관련있는 클래스 또는 인터페이스 등을 모아 하나의 묶음으로 단위를 구성한것
- 지금까지 클래스명에 패키지명을 함꼐 사용하지 않은 이유는 같은 패키지 안에서만 
사용했기 때문이다 그렇기 떄문에 서로 다른 패키지에 존재하는 클래스를 사용하는 경우에는
클래스명 앞에 패키지명을 명시해서 풀 클래스 이름으로 사용해야 한다.

### 임포트
- 서로 다른 패키지의 클래스를 사용할 때는 풀클래스 이름을 사용해야한다
- 하지만 매번 다른 클래스의 패키지명까지 기술 하기는 어려움으로 패키지명을 생략하기위해 임포트를 슨다
   ```ex)
  import com.ohgiraffers.section01.method.Calculator;
  
    /* static import의 경우 사용하려는 static method까지 전부 써줘야 한다. */
  
    import static com.ohgiraffers.section01.method.Calculator.maxNumberOf;
   ```
### API란
- 응용프로그램에서 사용할 있도록, 운영체제나 프로그래밍 언어가 제공하는 기능을 제어 할 수있도록 만든 인터페이스

### Math API
- 자주 쓰는 함수
-  Math.abs(절대값)
-  min(a,b): a 와 b중 더작은것
-  max(a,b): a 와 b중 더큰것
-  PI :원주율
-  random(): 난수 출력   
        ex) int rnadom=(int)(Math.random()*a)+b; b부터시작해서 a만큼인 수 안에 난수
            
    int random2=(int)(Math.random()*5)+1; 1부터 5까지의 수안에 난수
-  원하는 범위의 난수를 구하는 공식
 ```
        Random random = new Random();
		
		/* 목차. 1. 0 부터 9까지 난수 발생 */
		int randomNumber1 = random.nextInt(10);
		System.out.println("0 부터 9 까지의 난수 : " + randomNumber1);
 ```

### Scanner
- 콘솔 화면에서 값을 입력받아 출력해보기
- Scanner 객체생성
   ```
  Scanner 객체명= new Scanner(System.in);
    ```
- 자료형별 값 입력 받기
- 입력받을 때 안내 묵구는 별도로 출력해주지 않으니 작성해 줘야한다
  - print와 println은 차이가 있다
      ```    
            print일떄
          System.out.print("나이를 입력하세요 : ");
          int age = sc.nextInt();  // 나이를 입력하세요: (입력받는곳)
          System.out.println("입력하신 나이는 " + age + "입니다.");
            
            println일떄
          System.out.print("금액을 입력해주세요 : ");		//만약 안내 구문을 작성하지 않으면 그냥 멈춘것 처럼 보인다. 사실 기다리는 중이다.
          long money = sc.nextLong(); //금액을입력해주세요:
                                        (입력받는곳)
          System.out.println("입력하신 금액은 " + money + "원 입니다.");
      ```
- 자료형별 값받기
- nextInt : int형
- nextLine: String형
