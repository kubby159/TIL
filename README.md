# TIL

## CSS in JavaScript

자바스크립트에서 CSS를 컨트롤할 때 다음과 같이 작성한다.

1. querySelector를 이용해 원하는 HTML 태그를 가져온다.
2. 가져온 태그에 addEventListener를 붙여준다.
3. 그리고 원하는 동작을 함수 파라미터에 넘겨준다.(ex. click, resize etc..)
4. 두 번째 파라미터에는 동작 시 어떻게 동작할 지에 대한 함수를 넣어준다. 아래의 예시는 클릭 시 글씨색이 변하는 함수를 넘겨줬다.

```javascript
const h1 = document.querySelector("#title h1");

function handleTitleClick() {
  const currentColor = h1.style.color;
  let newColor;
  if (currentColor === "blue") {
    newColor = "tomato";
  } else {
    newColor = "blue";
  }
  h1.style.color = newColor;
}

h1.addEventListener("click", handleTitleClick);
```
