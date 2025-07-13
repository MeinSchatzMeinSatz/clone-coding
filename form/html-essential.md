# 양식(form)

## form

사용자로부터 입력을 받기 위한 양식을 작성하는 태그들을 통틀어 form이라고 합니다.

? 꼭 form 태그로 묶어 주어야 하나요?

-   form 태그는 입력한 데이터를 제출, 전송하기 위해 사용하는 태그입니다. 별도 제출할 필요가 없다면 form 태그를 사용하지 않으셔도 됩니다.

### method 속성

-   양식을 제출할 때 사용할 HTTP 메서드

1. Get 메서드

```
<form method="get" action="http://naver.com">
    <div>
        <label for="user-name">이름</label>
        <input id="user-name" type="text" name="name" />
    </div>
    <div>
        <label for="user-age">나이</label>
        <input id="user-age" type="number" name="age" />
    </div>
    <button type="submit">버튼</button>
</form>
```

양식 데이터를 action URL과 ?구분자 뒤에 이어 붙여서 전송.
GET 방식의 HTTP 요청은 브라우저에 의해 캐시되어 저장
보통 쿼리 문자열에 포함되어 전송되므로 길이의 제한이 있음(URL 길이제한은 브라우저마다 다름)
보안상 취약점이 존재하므로, 중요한 데이터는 POST 방식을 사용하여 요청

2. POST

-   폼 데이터를 별도로 첨부하여 서버로 전달하는 방식.
-   브라우저에 의해 캐시되지 않고, 브라우저 히스토리에도 남지 않음
-   POST 방식의 HTTP 요청에 의한 데이터는 쿼리 문자열과는 별도로 전송
-   데이터의 길이제한이 없고, GET 방식보다 보안성이 높음.

### enctype 속성

text/plain: 디버깅용 및 단순 텍스트 전송, 개발용으로만 사용 권장
application/x-www-form-urlencoded: 기본값(일반 텍스트만 전송)
multipart/form-data: 파일을 업로드할떄(<input type="file">이 존재하는 경우) 사용

### action 속성

양식 데이터를 처리할 프로그램의 URL을 적어줍니다.
데이터를 어디로 보낼것인지 지정합니다. 이 값은 반드시 유효한 URL이어야 합니다.
이 속성을 지정하지 않으면 데이터는 form이 있는 페이지의 URL로 보내집니다.

### autocomplete 속성

브라우저의 자동 완성 기능을 제어하는 속성입니다. 사용자가 이전에 입력했던 값을 브라우저가 기억하고 다시 제안할지 여부를 결정합니다.

-   off 자동입력 X
-   on 자동입력 O(기본값)

## input

### 공통 속성

name : input 양식 컨트롤의 이름 => 각 폼 요소에 고유한 이름을 부여
value : input 양식 컨트롤의 값 => 사용자가 입력한 값이나 기본 값을 나타낸다.
autocomplete : on/off 양식 자동완성 기능에 대한 힌트(check, radio 제외)
placeholder : 양식 전송을 위해 필수로 입력해야하는 값
required : 양식 전송을 위해 필수로 입력해야하는 값
disabled : 비활성화
readonly : 수정불가(읽기전용)

## label

=> 사용자 인터페이스 항목을 나타낸다.
input과 함께 사용할 것.

-   for-id를 이용해 연결하기
-   label 안에 input 중첩하여 연결하기

## select

옵션 메뉴를 제공합니다
multiple : 여러 개의 항목을 동시에 선택가능
size : 한번에 노출되는 항목의 수를 조절한다.
required : 선택 필수
disabled : 선택 불가

### option

메뉴의 각 옵션을 정의합니다.
모든 option은 자신이 선택되었을 때 값으로 사용할 value 속성이 필요합니다.
지정하지 않은 경우, option 내 텍스트 값으로 사용합니다.
selected 특성을 지정하면 해당 옵션을 선택한 상태로 페이지를 불러옵니다.
