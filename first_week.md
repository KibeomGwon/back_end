## 첫째주 요약본
---------
### 쿠키<br>
+ 쿠키: 서버가 클라이언트의 브라우저로 보내는 아주 작은 데이터<br>
+ 특징 : 키/값의 맵핑 구조, 유효기간이 있음 

+ http는 전 통신들의 정보를 기억하고 있지 않다 = stateless
http는 연결을 계속하고 있지 않다.<br>
여기서 서버에 접속기록, 정보 기록들을 알려주는 것이 쿠키<br> 
Ex)로그인을 했는데, 이 기록을 계속 유지하는 것은 쿠키가 있기 때문<br>
쿠키는 보안에 취약할 수 있기 때문에 httpOnly, secure같은 것을 활용해야함

+ 세션 저장소: 쿠키 들을 서버 측에서 보관해 주는 영역<br>
=> 통신할 때 세션id를 받아 정보(상태 데이터)를 기억함.

--------

### 네트워크

+ 네트워크: 두대 이상의 컴퓨터가 연결된 통신망<br>
+ 스위치: 하나의 네트워크 망 안에 있는 호스트(각각의 컴퓨터)들을 연결 시켜주는 장치<br>
+ 라우터: 다른 네트워크 망과 현재 네트워크 망을 연결 시켜주는 장치 (+ 스위치의 기능을 포함함)

+ Ip : internet protocol

+ ip주소 32bit를 4등분해서 주소 체계를 잡는데 4등분해서 나온 4byte 중 1byte를 옥텟(octet)이라고 한다

+ isp(internet service provider)가 공인ip를 공유기로 보내면 그 공유기에서 사설ip를 만들어서 공유기에 연결된 각각의 기기들에게 사설ip주소를 부여해 준다.

+ 컴퓨터 자기 자신을 가리키는 고유 (모든 컴퓨터에 약속된) ip주소는 ‘127.0.0.1’이다.<br> 이것을 localhost라고 부른다.

---------

### HTML,CSS,JAVASCRIPT
+ HTML : HyperText Markup Language<br>
HyperText : 문서간의 링크<br>
HTML은 내용을 구성하는 Word같은 역할을 한다.<br>
<여는 태그>내용</닫는 태그> 형태로 이루어진다.<br>

+ CCS : Cascading Style Sheets<br>
Cascading : 폭포처럼 떨어지는, 계단식의
=> 상위에서 하위로 떨어지는 식의 방식

+ JavaScript<br>
JavaScript != Java<br>
자바스크립트는 웹페이지에 이벤트를 발생 시키거나 사용자의 액션에 반응을 하게 만드는 언어이다.

+ 개발자 도구<br>
자신의 웹 브라우저에서 실행시킨 개발자 도구에서 html을 바꿔도 웹 브라우저에 있는 문서는 로컬에 복사된 문서를 실행시키는 것이기 때문에 바꿔도 서버에는 영향을 안준다.