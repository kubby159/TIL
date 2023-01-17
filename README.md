# TIL(2023.01.17)

## Event

- querySelector를 이용할 때 id 속성을 가진 태그를 가져오려면 '#'를, class 속성을 가진 태그를 가져오려면 '.'을 필수로 입력해줘야한다.
- console.dir(input) 을 해보면 여러 가지 input의 속성을 확인할 수 있는데 이번 시간에는 value를 확인하는 시간을 가졌고,
  input에 입력한 value를 console.log() 해봤다.
- 이벤트리스너 click 를 통해 클릭 시 input value 에 입력된 값을 출력할 수 있다.

```javascript
const loginForm = document.querySelector("#login-form"); // #login 안에 있는 요소를 탐색할 수 있음.
const loginInput = loginForm.querySelector("input"); // #login-form input
const loginButton = loginForm.querySelector("button");

function handleBtnClick() {
  console.log(loginInput.value);
  console.log("click");
}

loginButton.addEventListener("click", handleBtnClick);
```
