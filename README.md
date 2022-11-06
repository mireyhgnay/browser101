## 👉 Web APIs
window_size.html : 윈도우 사이즈 표기    
window_coordinates.html : 윈도우 좌표    
window_load.html : 윈도우 로드    


## 👉 Rabbit Script
```javascript
const button = document.querySelector('.button');
const rabbit = document.querySelector('#rabbit');

button.addEventListener('click', () => {
rabbit.scrollIntoView({ behavior: 'smooth', block: 'center'})
})
```
### element.scrollIntoView
[MDN](https://developer.mozilla.org/ko/docs/Web/API/Element/scrollIntoView)
- 화면의 특정 위치로 이동시켜주는 함수이다.
- element기반이기때문에 특정 element 를 기준으로 스크롤이 이동된다.

<사용 방법>
1. `element.scrollIntoView();`
    - 아무 매개변수도 사용하지 않고 그냥 사용하는 방법

2. `element.scrollIntoView(alignToTop);` // Boolean parameter
    - true/false 를 매개변수로 사용하는 방법
    - true : element요소의 **상단을 기준**으로 스크롤을 이동한다.
    - false : element요소의 **하단을 기준**으로 스크롤을 이동한다.
    ```javascript
    document.querySelector('.box').scrollIntoView(true); 
    document.querySelector('.box').scrollIntoView(false); 
    ```

3. `element.scrollIntoView(scrollIntoViewOptions);` // Object parameter
    -  options 객체를 넣어서 사용하는 방법 (⭐가장 많이 사용)
    - **behavior** : 전환 애니메이션 정의 (auto || smooth)
        - default : auto
        - smooth : 부드럽게 스크롤 이동
    - **block** : 수직 정렬 (start || center || end || nearest)
    - **inline** : 수평 정렬 (start || center || end || nearest)
