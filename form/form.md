# form 태그란.

form 태그는 입력요소(input, textarea, select 등)을 감싸서, 사용자가 입력한 데이터를 서버로 전송할 수 있게 도와줍니다.

```
// 기본구조
<form action="서버주소" method="전송방식">
 <!-- 입력 요소들-->
</form>
```

# form의 주요 속성

action : 데이터를 전송할 서버의 URL : action="/submit"
method : 전송 방식(GET 또는 POST) : method="post"
enctype : 데이터 인코딩 방식(파일 업로드 시 사용) : enctype="multipart/form-data"
autocomplete : 자동완성 사용 여부 : autocomplete="off"
target : 응답을 받을 창 지정 : target="\_blank"

# 대표적인 입력 요소

<input> : 텍스트, 비밀번호, 체크박스, 라디오 등 다양한 타입 지원
<textarea> ; 여러 줄 텍스트 입력
<select> : 드롭다운 목록
<button> : 버튼(전송, 초기화, 일반)

## input 태그의 주요 타입

text : 한 줄 텍스트 입력
password : 비밀번호 입력
email : 이메일 입력
number : 숫자 입력
checkbox : 체크박스
radio : 라디오 버튼
file : 파일 업로드
submit : 폼 제출
reset : 입력값 초기화

## form 관련 팁

label 태그를 사용하면 접근성이 좋아진다
'required' 속성으로 필수 입력을 지정할 수 있다.
'placeholder'로 입력 예시를 보여줄 수 있다.
'name' 속성은 서버에서 데이터를 구분하는 데 꼭 필요하다.
