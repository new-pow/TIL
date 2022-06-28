# [jQuery] 인덱스를 사용해 원하는 요소 선택하여 가져오기

## eq()
> 선택한 요소의 인덱스 번호에 해당하는 값을 찾는다. jQuery 객체 반환

### 문법 Syntax
```javascript
$("선택자").eq("숫자");
```

### 정의 Definition
- 선택한 요소의 형제 중 숫자를 통해 선택합니다.
- 음수를 설정하면 역순으로 선택합니다.
- 만약 인덱스 번호에 해당하는 요소가 없으면 null을 반환합니다.

### 활용 예시
```javascript
$moviePoster.each(function(index){
    let img = $img.eq(index);
    let movieInfo = $movieInfo.eq(index);
    $(this).on('mouseover',function(){
        img.css('opacity',0.4);
        movieInfo.css('opacity',1);
    })
    $(this).on('mouseout',function(){
        img.css('opacity',1);
        movieInfo.css('opacity',0);
    })
});
```

## get()
> 선택한 요소의 인덱스 번호에 해당하는 값을 찾는다. DOM개체 반환

### 문법 Syntax
```javascript
$("선택자").eq(숫자)
```

### 정의 Definition

> eq(), get()은 선택한 요소 중 N번째 요소를 반환하지만, 중요한 차이점이 있다.
>> - eq() : jQuery객체로 반환하며, jQuery메소드로 사용 가능하다.
>> - get() : DOM개체로 반환하며, jQuery메소드로 사용 불가능하다.

## index()
> 해당 요소의 index값을 가져온다.

```javascript
$("선택자").이벤트종류(function(){
	$("지정요소").index();
});
```


## 참고
---
[[jQuery] 인덱스 값을 사용해 원하는 위치의 요소를 선택 eq() / get() (21-05-19)](https://log.designichthus.com/61)