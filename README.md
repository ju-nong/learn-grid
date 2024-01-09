# learn-grid

##### 그리드 컨테이너 정의

```css
display: grid;
```

##### 그리드 트랙 크기 지정

```css
/* 1, 2, 3번 열에 200px 너비 지정 */
grid-template-columns: 200px 200px 200px;

/* 1, 2번 행에 100px 높이 지정  */
grid-template-rows: 100px 100px;
```

##### 그리드 트랙 크기 자동 지정

따로 크기가 지정되지 않은 트랙의 크기를 자동으로 지정

````css
grid-auto-columns: 100px;
grid-auto-rows: 100px;


##### 셀간의 간격
```css
/* 좌우 간격 */
row-gap: 20px;

/* 상하 간격 */
column-gap: 10px;

/* 좌우상하 간격 */
gap: 20px;

/* 좌우 상하 간격 */
gap: 20px 10px
````

##### 그리드에서 사용하는 함수 및 단위

repeat()

```css
/* 200px 200px 200px과 같음 */
grid-template-columns: repeat(3, 200px);
```

minmax()

```css
/* 높이의 최소값이 100px이고 최대값은 300px */
grid-auto-rows: minmax(100px, 300px);
```

fr (크기 단위)

```css
/* 너비 2 : 1 : 0.5 비율의 열을 갖는다 */
grid-template-columns: 2fr 1fr 0.5fr;

/* 100px를 빼고 남은 너비에서 1 : 2 비율을 할당 */
grid-template-columns: 100px 1fr 2fr;
```

auto (크기 단위)

```css
/* 높이의 최소값이 100px이고 최대값은 내용에 맞춤 */
grid-auto-rows: minmax(100px, auto);
```

auto-fill (개수 단위)

```css
/* 100px 너비를 가지며, 여백이 있다면 그대로 남김 */
grid-template-columns: repeat(auto-fill, minmax(100px, auto));
```

auto-fit (개수 단위)

```css
/* 100px 너비를 가지며, 여백이 있다면 셀들의 너비가 균등하게 늘어남 */
grid-template-columns: repeat(auto-fit, minmax(100px, auto));
```

##### 셀 영역 지정

end를 생략하면 1칸만 차지

```css
/* 1번째 ~ 2번째 열을 차지 */
grid-column-start: 1;
grid-column-end: 3;

/* 단축 문법 */
grid-column: 1 / 3;

/* 2번째 행을 차지 */
grid-row-start: 2;
grid-row-end: 3;

/* 단축 문법 */
grid-row: 2 / 3;
```

몇 칸을 차지할지 지정할 수 있음

```css
/* 1번째 ~ 2번째 열을 차지 */
grid-column: 1 / span 2;

/* 2번째 ~ 4번째 행을 차지 */
grid-row: 2 / span 3;
```

##### 그리드 영역 지정

규칙

1.  문자열 인자당 하나의 행
2.  각 영역은 띄어쓰기로 구분
3.  빈 영역은 .(개수 상관 없음)이나 none으로 정의

```css
/* 영역 지정 */
.grid-container {
    grid-template-area:
        "header header header"
        "a-side main b-side"
        ". ... none"
        "footer footer footer";
}

/* 영역 사용 */
.header{
   grid-area: header;
}

.a-side{
   grid-area: a-side;
}
...
```
