# [javascript] Map.prototype.forEach()

forEach() 함수는 입력한 순서에 따라 맵 오브젝트안에 있는 각각 키/값 쌍을 제공하는 기능을 실행합니다. 

## 문법
```javascript
myMap.forEach(callback[, thisArg])
```

### 파라미터

callback
: 각 요소들을 실행할 함수

thisArg
: 콜백함수를 실행할 때 사용할 값

### Return value

undefined.

## 설명

The forEach method executes the provided callback once for each key of the map which actually exist. It is not invoked for keys which have been deleted. However, it is executed for values which are present but have the value undefined.

callback is invoked with three arguments:

the element value
the element key
the Map object being traversed
If a thisArg parameter is provided to forEach, it will be passed to callback when invoked, for use as its this value.  Otherwise, the value undefined will be passed for use as its this value.  The this value ultimately observable by callback is determined according to the usual rules for determining the this seen by a function.

Each value is visited once, except in the case when it was deleted and re-added before forEach has finished. callback is not invoked for values deleted before being visited. New values added before forEach has finished will be visited.

forEach executes the callback function once for each element in the Map object; it does not return a value.

ExamplesEDIT
Printing the contents of a Map object

The following code logs a line for each element in an Map object:

function logMapElements(value, key, map) {
    console.log("m[" + key + "] = " + value);
}
new Map([["foo", 3], ["bar", {}], ["baz", undefined]]).forEach(logMapElements);
// logs:
// "m[foo] = 3"
// "m[bar] = [object Object]"
// "m[baz] = undefined"
SpecificationsEDIT
Specification	Status	Comment
ECMAScript 2015 (6th Edition, ECMA-262)
The definition of 'Map.prototype.forEach' in that specification.	Standard	Initial definition.
ECMAScript 2017 Draft (ECMA-262)
The definition of 'Map.prototype.forEach' in that specification.	Draft	 
Browser compatibilityEDIT
Desktop Mobile
Feature	Chrome	Firefox (Gecko)	Internet Explorer	Opera	Safari
Basic support	38	25.0 (25.0)	11	25	7.1
See alsoEDIT
Array.prototype.forEach()
Set.prototype.forEach()