# HTML `<input>` checked Attribute


## Example

선택된 체크박스가 포함된 폼의 HTML 코드

```html
<form action="demo_form.asp">
  <input type="checkbox" name="vehicle" value="Bike"> I have a bike<br>
  <input type="checkbox" name="vehicle" value="Car" checked> I have a car<br>
  <input type="submit" value="Submit">
</form>
```

## 정의 및 사용법

`checked` 속성은 부울 속성입니다. 

현재는, 그것이 <입력> 요소는 미리 선택해야 함을 지정하면 페이지가로드 될 때를 (확인). checked 속성은 <입력 유형 = "체크 박스">와 <입력 유형 = "라디오"> 사용할 수 있습니다. 검사 된 특성은 또한 자바 스크립트 페이지로드 후 설정 될 수있다.



The checked attribute is a boolean attribute.

When present, it specifies that an <input> element should be pre-selected (checked) when the page loads.

The checked attribute can be used with <input type="checkbox"> and <input type="radio">.

The checked attribute can also be set after the page load, with a JavaScript.

## 브라우저 지원

표의 수치는 완전히 특성을 지원하는 브라우저 버전을 나타냅니다.

|Attribute|  ![](http://www.w3schools.com/images/compatible_chrome.gif) |   |       |    |    |
|--|--|--|--|--|
|checked|	1.0|	2.0|	1.0|	1.0|	1.0|


## HTML 4.01 과 HTML5 에서의 차이점

없음


## HTML 과 XHTML 에서의 차이점

XHTML에서는 속성 최소화가 금지되어 있습니다.

checked 속성은 `<input checked="checked" />` 와 같이 지정해야 합니다.


## 문법

`<input checked>`