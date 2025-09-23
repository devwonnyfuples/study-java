# 1부: 자바 기술 시스템 소개
## 자바 기술 시스템
- 자바 가상 머신 위에서 동작하는 프로그래밍 언어 자바 기술 시스템에 속한다 : 코틀린, 클로저, JRuby, 그루비
- 요소
    - java programming language
    - java virtual machine 구현
    - class file format
    - java class library API
    - third party class library for another enterprise, open source
![alt text](/study-java/resources/얄코1.png)
![alt text](/study-java/resources/얄코2.png)
![alt text](/study-java/resources/얄코3.png)
![alt text](/study-java/resources/얄코4.png)
![alt text](/study-java/resources/얄코5.png)
![alt text](/study-java/resources/얄코6.png)
![alt text](/study-java/resources/얄코7.png)
![alt text](/study-java/resources/얄코8.png)
- JDK :
    - java programming language + java virtual machine + java class library
    - java 개발에 필요한 최소 환경

- JRE : 
    - java SE API + java virtual machine + 배포 기술
    - java program을 실행할 수 있는 표준 환경 제공

### 자바 기술 시스템 규성 요소
![자바 기술 시스템의 구성 요소](../resources/자바기술시스템의구성요소.png.png)

- 자바 언어 : 자바 언어
- 도구, api : java, javac, javadoc, jar, javap, JPDA, JConsole, java VisualVM, JMC, JFR, javaDB, 국제화, JVM TI,
IDL, 배포, 보안, trouble shooting, scripting, web service, RMI

- 배포 : java web start, 애플릿 java plugin

- 사용자 인터페이스 툴킷: swing, java 2d, AWT, 접근성, drag & drop, 입력기, 이미지 입출력, print service, sound

- 통합 library : IDL, JDBC, JNDI, RMI, RMI-IIOP, Scripting

- etc library : bean, 국제화 지원, input & output, JMX, JNI, 수학, networking, override mechanism, 보안, 직렬화, 확장 mechanism, XML JAXP

- 언어 및 유틸리티 기본 library : 언어 및 유틸리티, 컬렉션, 동시성 유틸리티, JAR, logging, 관리, 프레퍼런스 api, 참조 객체, 리플렉션, 정규식, 버저닝, Zip, 계측

- 자바 가상 머신: 자바 핫스팟 VM

---------------------------------------------
- 자바의 과거, 현재
- 자바 가상 머신 제품들
- 자바의 미래
### 실전
- 내 손으로 빌드하는 JDK


## 들어가며
자바는 프로그래밍 언어뿐 아니라, 여러가지 소프트웨어와 명세로 구성된 기술 시스템을 통칭한다.

## 자바의 탄생
- 1991년 4월: 제임스 고슬링 박사 : Green Project -> Oak

- 1995년 5월 23: Oak -> Java, 썬 마이크로시스템즈에서 처음 발표되었으며, 이후 오라클이 인수하여 현재까지 관리하고 있다. 자바는 플랫폼 독립성을 목표로 설계되었으며, "한 번 작성하면 어디서나 실행된다"는 슬로건으로 유명하다.

- 1996년 1월 23일 : JDK 1.0 출시
    - 자바 언어의 사용 공식: 런타임 환경 처음으로 마련
    - 가상 머신 : classic VM
        - 자바코드를 인터프리터 방식으로 실행
        - 인터프리터는 더 이상 동작을 하지 않았다
        - 당시에는 인터프리터와 컴파일러는 함께 구동되지 않음
           - 컴파일러를 사용하면, 코드 전체를 컴파일 해야 했음
               - 프로그램 응답 속도 : 너무 느려짐
               - 최적화 기법 적용 어려움


```text
java version "1.2.2"
Classic VM (build JDK-1.2.2-001, green threads, sunwjit)
```

- sun w jit
- Sun Workshop Jit : sun에서 제공한 플러그인 컴파일러

```text
devwonny@devwonnyui-MacBookAir ~ % java -version
openjdk version "22.0.1" 2024-04-16
OpenJDK Runtime Environment (build 22.0.1+8-16)
OpenJDK 64-Bit Server VM (build 22.0.1+8-16, mixed mode, sharing)
```

## 유년기
- 1997년 2월 19일 : JDK 1.1 출시
    - JAR 파일 포맷
    - JDBC
    - java beans
    - RMI
    - inner class
    - reflection

- 1999년 4월 27일 : hot spot virtual machine 출시
    - longview technologies 회사가 개발함
    - 1997년 Sun이 이 회사를 인수함

## 오픈 소스의 세계로
- 2006년 12월 11일: JDK 6 출시
    - 스크립트 언어 지원
    - 컴파일 타임 애너테이션 처리기
    - 마이크로 HTTP 서버 API 제공
    - 자바 가상 머신: LOCK, 동기화 구현, 가비지컬렉션, 클래스 로딩 개선

## 오라클의 품으로
- 2009년 2월 19일 : JDK 7 완성
   - Lambda : 람다식, 함수형 프로그래밍 지원 
   - jigsaw : 가상 머신 수준에서 모듈화 지원
   - 동적 언어 지원
   - G1 컬렉터 : 고성능 garbage collector
   - coin : java 구문의 세부 사항 개선

## 모던 자바 시작
- 2014년 3월 18일 : JDK 8
    - 람다식 지원
    - 나스혼 : 자바스크립트 엔진 내장
    - 새로운 시간 및 날짜 API
    - 핫스팟에서 영구 세대 완전 제거

-   자바는 주로 서버 사이드 애플리케이션, 모바일 애플리케이션, 임베디드 시스템 등 다양한 분야에서 사용된다.
자바 기술 시스템은 크게 다음과 같은 구성 요소로 이루어져 있다.
1. 자바 프로그래밍 언어: 자바 언어는 객체 지향 프로그래밍을 지원하며, 강력한 타입 검사와 자동 메모리 관리를 특징으로 한다.
2. 자바 개발 키트(JDK): JDK는 자바 애플리케이션 개발에 필요한 도구와 라이브러리를 포함한다. JDK에는 자바 컴파일러(javac), 자바 런타임 환경(JRE), 다양한 유틸리티 도구가 포함되어 있다.
3. 자바 런타임 환경(JRE): JRE는 자바 애플리케이션을 실행하는 데 필요한 환경을 제공한다. JRE에는 자바 가상 머신(JVM)과 표준 자바 클래스 라이브러리가 포함되어 있다.
4. 자바 가상 머신(JVM): JVM은 자바 바이트코드를 실행하는 가상 머신이다. JVM은 플랫폼 독립성을 제공하며, 다양한 운영 체제에서 자바 애플리케이션을 실행할 수 있도록 한다.
5. 표준 자바 클래스 라이브러리: 자바는 광범위한 표준 라이브러리를 제공하여, 데이터 구조, 네트워킹, 파일 입출력, 그래픽 사용자 인터페이스(GUI) 등 다양한 기능을 지원한다.
6. 자바 커뮤니티 프로세스(JCP): JCP는 자바 기술의 발전과 표준화를 담당하는 조직이다. JCP는 자바 명세 요청(JSR)을 통해 새로운 기능과 개선 사항을 제안하고 승인한다.
7. 자바 에코시스템: 자바는 풍부한 오픈 소스 라이브러리, 프레임워크, 도구를 포함하는 광범위한 에코시스템을 가지고 있다. 스프링(Spring), 하이버네이트(Hibernate), 아파치 톰캣(Apache Tomcat) 등은 자바 개발에 널리 사용되는 프레임워크와 서버이다.
자바 기술 시스템은 지속적으로 발전하고 있으며, 새로운 기능과 개선 사항이 정기적으로 추가되고 있다. 자바는 현재도 많은 개발자와 기업에서 널리 사용되고 있으며, 앞으로도 중요한 프로그래밍 언어로 자리매김할 것으로 예상된다.

## 1.4 자바 가상 머신 제품군


### 핫스팟 VM
- 기본 가상 머신
- 가장 널리 사용되는 자바 가상 머신
- longview technologies 작은 회사에서 개발함
핫스팟 VM(HotSpot VM)은 오라클이 개발한 자바 가상 머신으로, 자바 애플리케이션의 성능을 최적화하기 위해 설계되었다. 핫스팟 VM은 동적 컴파일과 가비지 컬렉션을 통해 실행 속도를 향상시키며, 다양한 최적화 기법을 적용한다. 핫스팟 VM은 자바 SE(Standard Edition)와 자바 EE(Enterprise Edition)에서 기본적으로 사용된다.

### 핫 코드 감지
- 컴파일했을 때 효과를 가장 크게 볼 수 있는 코드 영역을
- 런타임에 알아내어 JIT 컴파일러에 알려준다.
- JIT 컴파일러가 해당 코드를 메서드 단위로 컴파일 한다.
    - 메서드가 자주 호출되거나, 메서드 안에 시간을 잡아 먹는 순환문
    - JIT 컴파일 수행 -> stack 을 치환함
    - OST(온 스택 치환) : 런타임에 stack 을 치환 하는 기술
        - 컴파일 없이 즉시 실행
        - 일부 코드만 백그라운드에서 컴파일하여 치환


## 1.5 자바 기술의 미래
### 차세대 JIT 컴파일러
- 핫코드를 탐지 ---컴파일---> 네이티브 코드
- JIT 컴파일러의 출력 품질 -> 실행 효율 좌우

#### 핫스팟 가상 머신의 실행 서브 시스템
- JIT 컴파일러 2개 내장
    - C1(클라이언트 컴파일러) : 컴파일 속도가 빠름, 최적화를 적게함
    - C2(서버 컴파일러) : 컴파일 속도 느림, 최적화 더 많이 적용
- 인터프리터
- 그랄 컴파일러 (JDK 10부터 추가, JDK 16부터 독립) : C2 컴파일러를 대체할 목적
    - 장점
        - 컴파일 된 코드 출력 품질 높음
        - 개발 효율, 개발 확장성에서 C2보다 훨씬 훌륭

## 요즘 추세.. java 필요 없음
### 장시간 실행 할 필요 없음 || 크기 작은 application
- HelloWorld를 실행하려 해도 100MB가 넘는 JRB가 필요하다
- 마이크로서비스 아키텍처에서는 분할된 서비스 각각이 더 이상 수십에서 수백GB의 메모리를 쓸 일이 없다
    - 고가용성 서비스 클러스터를 활용하면 단일 서비스 를 24시간 중단 없이 실행하기 위해 노력할 이유가 줄어든다
    - 언제든지 중단하고 업데이트할 수 있기 때문이다
- 서버리스 아키텍처
   - 함수는 서비스보다 크기가 작고 실행 시간이 짧다. 
   - 현재 가장 널리 쓰이는 서버리스 런타임인 AWS 람다는 함수 실행 시간을 최장 15분까지만 허용한다.

### 이전 JDK
- 지금까지 자바 가상 머신
- 애플리케이션을 우선 실행 한후 
- JIT 컴파일러를 써서 빈번하게 실행되는 로직을 -> '네이티브 코드'로 바꿔 '실행' 했다. 

### 최근 JDK
- 애플리케이션 클래스 데이터 공유(Application Class Data Sharing, AppCD)
    - 로딩한 클래스 정보를 캐시해 두어 다음번 구동 시간을 줄 이는 기술
- AOT 컴파일
   - 애플리케이션을 실행하기 전에 '네이티브 코드'로 '컴파일' 함
   - 강점 :
       - 컴파일을 미리 해 두면 예열 과정을 건너뛰고 처음부터 '네이티브 코드'를 '실행'할 수 있다.
   - 단점 :
       - 한번 작성하면 어디서든 실행된다 약속을 지킬 수 없음
       - 하드웨어, 운영체제 별로 따로 컴파일 한 후 -> 배포 해야함
       - 컴파일 해야하는 코드에 대한 모든 것을 컴파일 time에서 알 수 있어야 한다.
       - 안그러면 JIT 컴파일로 돌아가야함...


### 프로젝트
#### 바할라
- 값 타입과 원시타입을 일반화한 제네릭 타입 제공 -> auto boxing, unboxing 필요 없다는 뜻
- 불변 타입, 명시적 선언 가능
- 비 참조 타입, 명시적 선언 가능

#### 파나마
- 자바 가상머신과 네이티브 코드의 경계를 허문다
- JNI를 이용해 java code -> 네이티브 코드 를 호출
    - 외부 함수
    - 메모리 API
    - vector API
    - Jextract : 네이티브 library header - java를 바인딩 해주는 도구