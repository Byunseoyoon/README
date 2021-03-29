# Github Flavered Markdown

## **1. Tables**
파이프 라인(|)을 이용해 테이블을 만들 수 있다.
- 작성방법
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

>*warning: 똑같이 내부에서 2번 이상의 띄어쓰기는 무시된다.*<br>
       *구분자 행 이후 아무것도 써있지 않으면 body가 없는 테이블이 만들어진다.*<br>
       *테이블 이후에 다른 블록과 구분하지 않고 markdown 코드를 쓰면 테이블이 무너진다*

<br>

### 1.1 정렬방법
2번째 줄에서 쓰이는 -- 부분을 구분자라고 하는데, 이 부분에서 콜론(:) 기호를 이용해 좌, 우, 중앙 정렬이 가능하다.

- 작성방법
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

- 작성방법
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
- 작성방법
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

- 작성방법<br>
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

>*참고: 들여쓰기를 통해 다중 업무 리스트도 만들 수 있다.*<br>
