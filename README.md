## ๐ Web APIs
window_size.html : ์๋์ฐ ์ฌ์ด์ฆ ํ๊ธฐ    
window_coordinates.html : ์๋์ฐ ์ขํ    
window_load.html : ์๋์ฐ ๋ก๋    


## ๐ Rabbit Script
```javascript
const button = document.querySelector('.button');
const rabbit = document.querySelector('#rabbit');

button.addEventListener('click', () => {
rabbit.scrollIntoView({ behavior: 'smooth', block: 'center'})
})
```
### element.scrollIntoView
[MDN](https://developer.mozilla.org/ko/docs/Web/API/Element/scrollIntoView)
- ํ๋ฉด์ ํน์  ์์น๋ก ์ด๋์์ผ์ฃผ๋ ํจ์์ด๋ค.
- element๊ธฐ๋ฐ์ด๊ธฐ๋๋ฌธ์ ํน์  element ๋ฅผ ๊ธฐ์ค์ผ๋ก ์คํฌ๋กค์ด ์ด๋๋๋ค.

<์ฌ์ฉ ๋ฐฉ๋ฒ>
1. `element.scrollIntoView();`
    - ์๋ฌด ๋งค๊ฐ๋ณ์๋ ์ฌ์ฉํ์ง ์๊ณ  ๊ทธ๋ฅ ์ฌ์ฉํ๋ ๋ฐฉ๋ฒ

2. `element.scrollIntoView(alignToTop);` // Boolean parameter
    - true/false ๋ฅผ ๋งค๊ฐ๋ณ์๋ก ์ฌ์ฉํ๋ ๋ฐฉ๋ฒ
    - true : element์์์ **์๋จ์ ๊ธฐ์ค**์ผ๋ก ์คํฌ๋กค์ ์ด๋ํ๋ค.
    - false : element์์์ **ํ๋จ์ ๊ธฐ์ค**์ผ๋ก ์คํฌ๋กค์ ์ด๋ํ๋ค.
    ```javascript
    document.querySelector('.box').scrollIntoView(true); 
    document.querySelector('.box').scrollIntoView(false); 
    ```

3. `element.scrollIntoView(scrollIntoViewOptions);` // Object parameter
    -  options ๊ฐ์ฒด๋ฅผ ๋ฃ์ด์ ์ฌ์ฉํ๋ ๋ฐฉ๋ฒ (โญ๊ฐ์ฅ ๋ง์ด ์ฌ์ฉ)
    - **behavior** : ์ ํ ์ ๋๋ฉ์ด์ ์ ์ (auto || smooth)
        - default : auto
        - smooth : ๋ถ๋๋ฝ๊ฒ ์คํฌ๋กค ์ด๋
    - **block**ย : ์์ง ์ ๋ ฌ (start || center || end || nearest)
    - **inline**ย : ์ํ ์ ๋ ฌ (start || center || end || nearest)
