# Back-end-road-map

<br>

### 인터넷
- 네트워크의 집합체
- n개의 컴퓨터들을 연결하기위해 라우터를 이용한다.
- 웹 소켓 : 데이터를 주고받을 때 HTTP로 통신. HTTP위에서 동작

<hr>

### Git
- 분산형 버전관리 시스템
- 협업가능
- 구조
    - 작업 디렉토리
    - 스테이지 에어리어
    - 레퍼지토리
- 동작순서 : 작업 디렉토리 -> add -> 스테이지 에어리어 -> commit -> 레퍼지토리

Github : 원격저장소

<hr>

### JSON 
- javascript object notation
- 자바스크립트 오브젝트 표현법에서 온 표현법
- 주석사용 불가 
- 표현방식
    - Object {string, key : value}
    - Array { (whitespace), value}
    - Value = string, number, object, array, true, false, null

참고 https://json.org/json-ko.html

### YAML
- JSON보다 방법이 다양하다.

참고 https://learnxinyminutes.com/docs/yaml/

<hr>

### 리눅스 명령어
- pwd: 현재위치 출력
- ls : 현재 디렉토리의 파일과 디렉토리들을 보여줌
- cd : cd (이동할 디렉토리 명)
- rm : rm (삭제할 파일)
- cat : cat (내용을 확인할 파일)
- touch : touch (만들 파일 명) 
    - 파일 명으로 빈 파일이 생성됨.
- echo : echo "(출력할 문자)"
- ip addr, if config : 아이피 정보 확인
- ss : 네트워크 정보 확인
- nc : 서버의 포트번호를 확인
- which : which (명령어)
    - 명령어의 위치를 알려줌
- tail : tail (파일명)
    - 파일 마지막 부분을 출력해 줌
- find : find (파일, 디렉토리)
    - 파일이나 디렉토리를 찾아줌
- ps : ps, ps aux
    - 프로세스 상태를 보여줌
- grep : grep "(찾을 패턴)" (파일명)
    - 파일 안에서 패턴을 찾아 줌
- kill : kill (pid)
    - 프로세스를 죽이는 명령어

<hr>

### 웹서버 ( 리버스 프록시 )
- 유저와 웹 어플리케이션 서버 사이에 자리하고 있음
- 요청 : 유저 -> request -> web server -> web app server
- 응답 : 유저 <- reponse <- web server <- web app server
- 대표적 제품 
    - 엔진
    - IIS
    - Apache

<hr>

### 인증과 인가
- 인증 (Authentication) : 누구인지 확인해 주는 것
- 인가 (Authorization) : 무엇을 할 수 있는지 확인해 주는 것

<hr>

### 프레임워크
- 개발시에 필요한 것들을 미리 만들어 주어서 작업을 편하게 만들어주는 코드덩어리
- 2가지 종류
    - 개발시에 설정과 코드 작성에 제한을 두는 프레임워크
    - 최소한의 코어만을 가지고 설정과 제약을 조금만 하는 프레임워크

<hr>

### 데이터베이스 (데이터 베이스 소프트웨어를 통징)
- rdb : relational database , 관계형 데이터베이스
    - 데이터를 행과 열로 이루어진 테이블로 관리
    - 기본키를 사용하여 각 행을 식별
    - 각 테이블 간의 관계를 지을 수 있다.
- NoSql (No Sql, Not only Sql)
    - sql 뿐만이 아니라 다른 것들도 더 쓴다.
    - Sql이 아니다
    - rdb에 비해서 분산서버가 잘 되어있다.
- ORM (Object relation mapping)
    - 클래스 오브젝트와 테이블의 관계를 클래스로 가져올 수 있도록 해주는 프로그램
- ACID
    - 원자성
    - 일관성
    - 격리성
    - 내구성
- 트랜잭션
    - 데이터베이스의 상태변화를 시키기 위해서 수행하는 작업의 단위
    - 동시다발적으로 발생하는 데이터의 변경 중에도 DB의 데이터가 안정적으로 변경될 수 있도록 하게 함
- N + 1
    - ORM에서 많이 발생
    - 다른 클래스와 관계 설정이 되어있는 클래스를 조회할 때 데이터 개수만큼 쿼리가 발생하는 것

<hr>

### API
- REST, GraphQl 방식으로 작성
- REST ( Representational State Transfer ) 표현적 상태 전달자 = 자원의 표현에 의한 상태 전달
- 자원은 HTTP URI 방식으로 표현
- HTTP Method를 사용하여 해당자원에 대한 상태를 전달
    - POST,GET,PUT,DELETE
- GraphQL
    - 쿼리언어
    - 클라이언트가 서버로부터 데이터를 효과적으로 가져오게 하는 것이 목적
    - endpoint가 하나만 있음 ( 하나의 url을 가지고 계속 통신하는 것을 의미 )
    - 클라이언트가 서버에 쿼리를 날리는 개념
    - json형태로 되어있음
- 현업에서는 REST, GraphQL을 둘 다 사용하여 혼합해서 씀.

<hr>

### 배치처리
- 일정기간 동안 데이터를 모아두었다가 대량의 데이터작업을 한번에 하는 것을 의미
- 일정 시간마다 주기적으로 실행해야 하는 작업을 의미하기도 함
    - 스케줄링을 해서 작업을 처리
    - 가장 간단한 방법으로 운영체제의 스케줄링 방법으로 처리하는 방법도 있음.
        - Linux의 crontab
        - 윈도우의 작업 스케줄러
- 다른 툴
    - Jenkins 배치처리
    - 스프링 배치

<hr>

### 배포하기
- CI / CD : 지속적으로 통합, 지속적으로 배포
- CI : 배포 전의 작업을 자동화
    - 코드 병합, 코드 빌드, 코드 테스트
- CD : 배포하는 것을 고도화하는 것
    - 롤링배포 : 서버 여러 대 중에 몇 대만 계속 돌아가면서 배포하는 것
    - 블루 / 그린 배포 : 똑같은 수의 서버를 미리 다 띄어두고 주소만 바꿔치기하는 배포
    - 까나리 배포 : 특정 퍼센트의 서버에만 배포한 다음 문제가 없으면 점차 배포를 늘려가는 배포
<hr>

### 그 외
- 도커
- OAuth
- 클라우드
- 보안

