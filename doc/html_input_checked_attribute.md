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

The checked attribute is a boolean attribute.

When present, it specifies that an <input> element should be pre-selected (checked) when the page loads.

The checked attribute can be used with <input type="checkbox"> and <input type="radio">.

The checked attribute can also be set after the page load, with a JavaScript.

Browser Support
The numbers in the table specify the first browser version that fully supports the attribute.

Attribute					
checked	1.0	2.0	1.0	1.0	1.0
Differences Between HTML 4.01 and HTML5
NONE.

Differences Between HTML and XHTML
In XHTML, attribute minimization is forbidden, and the checked attribute must be defined as <input checked="checked" />.

Syntax
<input checked>