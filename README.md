# Github Flavered Markdown
GFM 확장된 파트
___
## **1. Tables**
파이프 라인(|)을 이용해 테이블을 만들 수 있다.
- **작성방법**
```
|이름|나이|성별|
|--|--|--|
|홍길동|20|남|
|James|21|여|
```
- ***example***

|이름|나이|성별|
|--|--|--|
|홍길동|20|남|
|James|21|여|

>*warning : 똑같이 내부에서 2번 이상의 띄어쓰기는 무시된다.*<br>
       *구분자 행 이후 아무것도 써있지 않으면 body가 없는 테이블이 만들어진다.*<br>
       *테이블 이후에 다른 블록과 구분하지 않고 markdown 코드를 쓰면 테이블이 무너진다*

<br>

### 1.1 정렬방법
2번째 줄에서 쓰이는 -- 부분을 구분자라고 하는데, 이 부분에서 콜론(:) 기호를 이용해 좌, 우, 중앙 정렬이 가능하다.

- **작성방법**
```
|좌|중앙|우|
|:--|:--:|--:|
|왼쪽 정렬|중앙 정렬|오른쪽 정렬|
```
- ***example***

|좌|중앙|우|
|:--|:--:|--:|
|왼쪽 정렬|중앙 정렬|오른쪽 정렬|

<br>

### 1.2 공백 및 초과
자료가 써진 행의 열수 > 첫행 열수 : 초과된 자료는 무시된다. 반대의 경우, 빈칸에 공백이 들어간다.

- **작성방법**
```
| abc | def |
| --- | --- |
| bar |
| bar | baz | boo |
```
- ***example***

| abc | def |
| --- | --- |
| bar |
| bar | baz | boo |

<br>

### 1.3 구분자
구분자의 개수는 1개 이상 사용할 수 있고, 한 행에서 제일 앞과 뒤의 파이프라인(|)은 생략이 가능하다.
- **작성방법**
```
| abc | defghi |
:-: | -----------:
bar | baz
```
- ***example***

| abc | defghi |
:-: | -----------:
bar | baz

<br>

___
## 2. Task List
업무 리스트와 체크 여부를 만들 수 있다.

- **작성방법**<br>
하이픈(-) 이후에 대괄호를 쓰고 그 안을 공백 or x로 채운 뒤 할 일을 작성한다.
```
- [ ] 끝내주게 숨쉬기
- [x] 고급지게 잠자기
   - [x] 배터지게 밥먹기
```

- ***example***

- [ ] 끝내주게 숨쉬기
- [x] 고급지게 잠자기
   - [x] 배터지게 밥먹기

>*참고 : 들여쓰기를 통해 다중 업무 리스트도 만들 수 있다.*

<br>

___
## 3. Strikethrough
물결표시(~)를 이용해 취소선을 만들 수 있다. 

|작성방법|Example|
|--|:--|
|\~\~gihub~~ markdown|~~gihub~~ markdown|

>*참고 :~~ 강조 구문 내에서 엔터 두 번으로 단락이 새로 생성되면 취소선이 사라진다.*

<br>

___
## 4. Autolinks
꺽새 없이 자동링크를 달 수 있다.<br>
자동 링크는 선의 시작 부분, 공백 뒤 또는 구분자(\*, \_, \~, \))에만 사용할 수 있다.<br>

### 4.1 URL
유효한 도메인은 영숫자 세그먼트, 밑줄(\_) 및 하이픈(\-), 마침표(.)로 구성되어 있다.**( 마침표(.)는 하나 이상 있어야 함 )**
- ***참고사항***

|설명|Example|
|--|:--|
|http는 자동으로 삽입 가능|www.markdownguide.org/extended-syntax/|
|도메인 이후 문자 삽입 가능|Visit www.google.co.kr for more information.|
|후행 구두점은 자동 링크의 일부로 간주 X | Visit www.google.co.kr.|
|자동 링크가 ')'로 끝날 때 <br>전체 링크에서 일치하지 않는 괄호 부분을 자동링크로 간주 X|  www.google.com/search?q=Markup+(business)<br>www.google.com/search?q=Markup+(business)))<br>(www.google.com/search?q=Markup+(business))<br>(www.google.com/search?q=Markup+(business)|
|자동 링크 내부에 괄호가 있는 경우 위의 규칙 적용 X|www.google.com/search?q=(business))+ok|
|'<'는 자동링크 즉시 종료|www.commonmark.org/he<lp|

<br>

### 4.2 Email
텍스트 노드 내에서 이메일 주소가 인식되면 이메일이 자동링크가 된다.
- **인식조건**
```
  -  영숫자 또는 '., -, _, +'인 하나 이상의 문자
  -  '@' 기호
  -  적어도 하나의 마침표(.)가 있어야 한다. 
  -  마지막 문자는 '-' 또는 '_' 중 하나로 끝나면 안된다.
```

- ***example***<br>
bsy4943@naver.com

- ***참고사항***

|설명|Example|
|:--|:--|
|'+'는 '@' 앞에 올 수 있지만, '@' 후에 올 수 없다.| hello@mail+xyz.example<br>hello+xyz@mail.example|
|'마침표(.), 하이픈(-), 언더바(\_)'는 @의 양쪽에서 사용할 수 있으나,<br> 전자 메일 주소 끝에는 '마침표(.)'만 사용할 수 있다.| a.b-c_d@a.b<br>a.b-c_d@a.b.<br>a.b-c_d@a.b-<br>a.b-c_d@a.b_|

<br>

___
## 5. Disallowed Raw HTML
GFM은 태그 필터 확장을 활성화하며, 여기서 HTML 출력을 렌더링할 때 아래 HTML 태그들은 앞에 있는 '<'가 '\&lt;'로 대체되어 필터링이 된다.
- **tagfilter**
```
- <title>
- <textarea>
- <style>
- <xmp>
- <iframe>
- <noembed>
- <noframes>
- <script>
- <plaintext>
```

- **example**
```
<strong> &lt;title> <style> <em>

<blockquote>
  <xmp> is disallowed.  <XMP> is also disallowed.
</blockquote>
```
위의 리스트에 있는 '<'만 HTML 출력을 렌더링할 때 '\&tl;'로 필터링 된다.(위의 태그들 이외의 다른 모든 HTML태그들은 그대로 유지됨)
```
<p><strong> &lt;title> &lt;style> <em></p>
<blockquote>
  &lt;xmp> is disallowed.  &lt;XMP> is also disallowed.
</blockquote>
```
> 이러한 태그들은 특히 HTML이 고유의 방식으로 해석되는 방법을 변경할 때 선택된다(즉, 중첩된 HTML은 다르게 해석됨).<br>
> 일반적으로 다른 렌더링된 Markdown 컨텐츠의 맥락에서 바람직하지 않다.<br>
