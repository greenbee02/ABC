# mermaid 실 습 
-순서도 실습
    -첫번째 샘플

```mermaid
classDiagram
    class Person{
        +name:str
        +phoneNumber:str
        +emailAddress:str
        +purchaseParkingPass()
    }
    class Address{
        +street:str
        +city:str
        +state:str
        +postalCode:int
        +country:str

        -clidate():bool
        +outputAsLabel():str
    }
    class Student{
        +studentNumber:int
        +averageMark:int
        +isEligibleToEnroll(str):bool
        +getSeminarsTaken():int
    }
    
```

```mermaid
sequenceDiagram
    actor 홍길동
    actor 이순신
    홍길동 ->> 이순신: 안녕하세요?
    이순신 ->> 홍길동: 반갑습니다.
```

```mermaid
sequenceDiagram
    participant A as 프로세서
    participant B as 데이터베이스
    A ->> B: DB 접속 요청
    B ->> A: 접속 승인
```

```mermaid
sequenceDiagram
    actor A as 사용자
    participant B as 인증 시스템
    A --> B: 아이디/비밀번호 입력
    activate B
    B -> A: 인증완료
    deactivate B
```

```mermaid
sequenceDiagram
    actor A as 사용자
    participant B as 인증 시스템
    A ->>+ B: 아이디/비밀번호 입력
    A ->>+ B: catcha 입력
    B -->>- A: catcha 성공
    B -->>- A: 인증 완료
```

```mermaid
sequenceDiagram
    autonumber
    actor A as 사용자
    participant B as 인증 시스템
    A ->>+ B: 아이디/비밀번호 입력
    A ->>+ B: catcha 입력
    B -->>- A: catcha 성공
    B -->>- A: 인증 완료
```

```mermaid
sequenceDiagram
    participant A as Data Updater
    participant B as DB
    loop 1시간마다 수행
        A ->> B: send update data
        B -->> A: update result
    end
```

```mermaid
sequenceDiagram
    actor A as 사용자
    participant B as 서버
    
    A ->> B: 서비스 상태 요청
    
    alt 가능
        B -> A: 서비스 가능 상태입니다.
    else 불가능
        B -> A: 현재 서비스 중단 상태입니다.
    else 점검중
        B -> A: 점검중... 기다려 주세요
    end
```

```mermaid
sequenceDiagram
    par 강감찬 to 이순신
        강감찬 ->> 이순신: 안녕하세요?

    and 강감찬 to 홍길동
        강감찬 ->> 홍길동: 안녕하세요?
    end
    
    이순신 -->> 강감찬: 강 장군! 오랜만이오.
    홍길동 -->> 강감찬: 장군님, 홍길동 여기 있습니다.
```

```mermaid
sequenceDiagram
    participant A as User
    participant B as Client
    participant C as Sever
    participant D as Database

    A ->> B: Fill username
    A ->> B: Fill password
    B ->> A: Enable "Login" button
    A ->> B: Click "Login" button
    B ->>+ C: POST/login
    C ->>+ D: SELECT FROM users
    Note over C,D: See login.py for impl. details
    D -->>- C: result
    C -->>- B: {authenticated:true}
    B ->> A: redirect/home

```

```mermaid
classDiagram
    class BankAccount
    BankAccount: String owner
    BankAccount: Bigdecimal balance
    BankAccount: deposit(amount)
    BankAccount: withdrawal(amount)
```

```mermaid
classDiagram 
    Animal <|--  Dog
```

```mermaid 
classDiagram 
    class BankAccount{
        +String owner$
        -Int 잔액
        +deposit(금액)* int
        +withdrawl(금액)$ int
    }
```

```{mermaid}
classDiagram 
    classA <|-- classB
    classC *-- classD
    classE o-- classF
    classG <-- classH
    classI <.. classJ
    classK <|.. classL
    classM -- classN
    classO .. classP
```

```{mermaid}
classDiagram
    Course "1..*" <-- "1" Student  
```

```{mermaid}
classDiagram
    class Color{
        <<enumberation>>
        RED
        GREEN
        BLUE
        WHITE
        BLACK
    }
```




```mermaid
ClassDiagram 
    class
        Person: +name:str
        Person: +phoneNumber:str
        Person: +emailAddress:str
        Person: +purchaseParkingPass()
```  


```mermaid
flowchart 
    id1([밥을 먹지 않았다])
    id2{{String status = hunger \n Strubg food = nothing}}
    id3{배가 고픈가?}
    id4{먹을 것이 있는가?}
    id01[안먹는다]
    id02[먹지 않는다]
    id5[밥을 먹는다]
    id6[밥을 먹었다!]
    id7([   END   ])
    id03[배불러]
    id1 --> id2{{String status = hunger \n Strubg food = nothing}}
    

    id2 --> id3
    id3 -->|YES| id4
    id3 -->|NO| id03
    id03 --> id01
    id4 -->|NO| id01
    id01 -->|출력| id02
    id02 --> id7
    id4 -->|YES| id5
    id5 --> id6
    id6 --> id7

```


```mermaid

flowchart 
    A[설날 아침] -->|세뱃돈| B(쇼핑 가기)
    B --> C{뭘 사야하나?}
    C -->|선택1| D[노트북]
    C -->|선택2| E[스마트폰]
    C -->|선택3| F[자동차] 
```
## 여기는 수업 끝 입니다
    