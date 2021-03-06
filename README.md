# Trillio Flexbox (Udemy Advanced CSS and Sass)

# ๐ Overview

- flex-basis, flex-grow๋ก ์ฝ๊ฒ ๋น์จ์ ๋๋๊ธฐ
- align-items: stretch ๊ฐ ๊ธฐ๋ณธ๊ฐ ์์ ์๊ธฐ
  - ์ปจํ์ด๋ ๋ด๋ถ์ ์์ดํ๋ค์ด cross axis ์ถ ๋ฐฉํฅ์ผ๋ก ๊ธธ์ด / ๋๋น๊ฐ ๊ฐ์์ง์ ์ดํด
- align-self ์์ฑ์ผ๋ก ์์ดํ ๊ฐ๋ณ์ ์ผ๋ก cross axis ์ถ์ ์ ๋ ฌ์ ๊ฒฐ์ ํ  ์ ์์
- flex์ margin: auto ์์ฑ์ผ๋ก space-between๊ณผ ๊ฐ์ ํจ๊ณผ๋ฅผ ์ป๊ธฐ
- ๋์์ธ ์ฌ์ฌ์ฉ์ฑ์ ๋์ฌ์ฃผ๋ ์์ฑ๋ค.. `inherit, currentColor, transparent`
- flex-wrap, flex-basis ์์ฑ์ผ๋ก n-column layout ๋ง๋ค๊ธฐ
- box-sizing: content-box๋ border ๋๋ฌธ์ ๋ด๋ถ ํฌ๊ธฐ๊ฐ ์ค์ด๋๋ ๋ฌธ์ ๋ฅผ ํด๊ฒฐํ๋ค.
- SVG ํ์ผ์ ์ฌ์ฉํ๊ธฐ
  - sprite.svg ํ๋์ ์ด๋ฏธ์ง๋ก ์ฌ๋ฌ ์์ด์ฝ์ ์ฌ์ฉํ  ์ ์๋ค.
  - fill: var(--color-grey-dark-3); ๋ก ์์์ ๋ณ๊ฒฝํ  ์ ์๋ค
  - background-image๋ก svgํ์ผ์ ๊ฐ์ ธ์ค๋ ๋ฐฉ์๊ณผ mask ํ๋กํผํฐ ์ฌ์ฉํ๊ธฐ
- flex box ์ ๋ฐ์ํ
  - side by side ๋ฐฐ์น๋ฅผ ์ ์๋๋ก
  - wrap์ผ๋ก ๋จ์ด๋จ๋ฆฌ๊ธฐ๋ ํ๋ค.
  - ๋ฐ๋๋ก side by side ๋ฅผ ์ ์ฉํ๊ณ  ๋ด๋ถ ์์ดํ์ ๊ท ๋ฑํ ํฌ๊ธฐ๋ฅผ ๊ฐ๋๋ก ํ  ์ ์๋ค.

---

# ๐ Contents

## ํ๋ ์ค ๋ ์ด์์์ ์ดํด

### ๐ flex-basis, flex-grow๋ก ์ฝ๊ฒ ๋น์จ์ ๋๋๊ธฐ

```css
.sidebar {
  flex: 0 0 18%; /* 18% */
}

.hotel-view {
  flex: 1; /* 82% */
}
```

### ๐ align-self ์์ฑ์ผ๋ก ์์ดํ ๊ฐ๋ณ์ ์ผ๋ก cross axis ์ถ์ ์ ๋ ฌ์ ๊ฒฐ์ ํ  ์ ์์

```css
  .user-nav {
    display: flex; /* flex ์ปจํ์ด๋์ด์ */
    align-items: center;  /*(์์ดํ๋ค์ ์์ง ๊ฐ์ด๋ฐ ์ ๋ ฌํจ)*/
    align-self: stretch; /* flex ์์ดํ์ด๋ค.(์์ ์ ๋๋ฆฌ๊ณ )*/
```

### ๐ align-items: stretch ๊ฐ ๊ธฐ๋ณธ๊ฐ ์์ ์๊ธฐ;๐ flex์ margin: auto ์์ฑ์ผ๋ก space-between๊ณผ ๊ฐ์ ํจ๊ณผ๋ฅผ ์ป๊ธฐ

```css
&__stars {
  /*MEMO: flex: 1์ ํ๋ฉด ์์์ ํฌ๊ธฐ๊ฐ ๋์ด๋๊ธฐ ๋๋ฌธ์, hover ์ด๋ฒคํธ ์ ์ ์ฉ ์์ญ์ด ๋๋ฌด ์ปค์ง๋ค.*/
  /* flex: 1 ;*/
  /* MEMO: ์์ ์์์ ๊ฑฐ๋ฆฌ๋ฅผ ์ต๋ํ ๋ฒ๋ฆฌ๊ธฐ ์ํด์ margin: auto๋ฅผ ์ฌ์ฉํ๋ค. ์๋์ผ๋ก ๊ณ์ฐํ์ฌ ์ต๋ํ margin์ ์ฃผ๊ฒ๋จ.*/
  margin-right: auto;
  /* MEMO: SVG img๋ค์ ๋์ด๋ฅผ ๊ฐ๊ฒ ํด์ฃผ๊ธฐ ์ํด ๋ถ๋ชจ ์์์ flex๋ฅผ ์ ์ฉ์์ผ์ฃผ์๋ค.*/
  display: flex;
}
```

### ๐ flex-wrap, flex-basis ์์ฑ์ผ๋ก n-column layout ๋ง๋ค๊ธฐ

```css
display: flex;
flex-wrap: wrap;

&__item {
  flex: 0 0 50%; /* 2-column ์ผ๋ก ๋ฐฐ์น๋๋ค. */
  margin-bottom: 0.7rem;
}
```

## ํ๋ ์ค ๋ ์ด์์๊ณผ ๋ฐ์ํ์ ์กฐํฉ

### ๐ side by side ๋ฐฐ์น๋ฅผ ์ ์๋๋ก ๋ฐ๊พธ์ด์ฃผ๊ธฐ

```css
@media only screen and (max-width: $bp-medium) {
  flex-direction: column;
}
```

### ๐ wrap์ผ๋ก ๋จ์ด๋จ๋ฆฌ๊ธฐ๋ ํ๋ค.

```css
@media only screen and (max-width: $bp-smallest) {
  flex-wrap: wrap;
  align-content: space-around;
  height: 11rem;
}
```

### ๐ ๋ฐ๋๋ก side by side ๋ฅผ ์ ์ฉํ๊ณ  ๋ด๋ถ ์์ดํ์ ๊ท ๋ฑํ ํฌ๊ธฐ๋ฅผ ๊ฐ๋๋ก ํ  ์ ์๋ค.

```css
  .side-nav {
    /* ์๋ต */
    @media only screen and (max-width: $bp-medium) {
      display: flex;
      margin: 0;
    }

    &__item {
      position: relative;

      &:not(:last-child) {
        margin-bottom: 0.5rem;

        @media only screen and (max-width: $bp-medium) {
          margin: 0;
        }
      }

      @media only screen and (max-width: $bp-medium) {
        flex: 1;
      }
    }
```

## ๊ธฐํ ํ

### ๐ SVG ํ์ผ์ ์ฌ์ฉํ๊ธฐ

- id๋ฅผ #์ผ๋ก ๊ตฌ๋ถํ์ฌ ๋ถ๋ฌ์จ๋ค.

  ```html
  <svg
    style="position: absolute; width: 0; height: 0; overflow: hidden;"
    version="1.1"
    xmlns="http://www.w3.org/2000/svg"
    xmlns:xlink="http://www.w3.org/1999/xlink"
  >
    <defs>
      <symbol id="icon-bookmark" viewBox="0 0 20 20">
        <title>bookmark</title>
        <path
          class="path1"
          d="M14 2v17l-4-4-4 4v-17c0-0.553 0.585-1.020 1-1h6c0.689-0.020 1 0.447 1 1z"
        ></path>
      </symbol>
      <symbol id="icon-chevron-down" viewBox="0 0 20 20">
        <title>chevron-down</title>
        <path
          class="path1"
          d="M4.516 7.548c0.436-0.446 1.043-0.481 1.576 0l3.908 3.747 3.908-3.747c0.533-0.481 1.141-0.446 1.574 0 0.436 0.445 0.408 1.197 0 1.615-0.406 0.418-4.695 4.502-4.695 4.502-0.217 0.223-0.502 0.335-0.787 0.335s-0.57-0.112-0.789-0.335c0 0-4.287-4.084-4.695-4.502s-0.436-1.17 0-1.615z"
        ></path>
      </symbol>
    </defs>
  </svg>
  ```

  ```html
  <svg class="user-nav__icon">
    <use xlink:href="img/sprite.svg#icon-bookmark"></use>
  </svg>

  <svg class="user-nav__icon">
    <use xlink:href="img/sprite.svg#icon-chat"></use>
  </svg>
  ```

  ```css
  fill: var(
    --color-grey-dark-3
  ); /* mark up ํ svg ์ด๋ฏธ์ง๋ fill ๋ก ์์์ ๋ณ๊ฒฝํ  ์ ์๋ค. */
  ```

- css ์์ background-image๋ก svg ์ฌ์ฉํ๊ธฐ

  - background-image๋ก svgํ์ผ์ ๊ฐ์ ธ์ค๋ ๋ฐฉ์(old browser)์ ์์ ๋ณ๊ฒฝ์ด ๋ถ๊ฐ๋ฅํ๋ค -> mask๋ฅผ ์ฌ์ฉํ๋ค.
  - mask css image ๋ถ๋ถ๋ง ๋นต๊พธ๋ฝ(newer browser)ํด์ ์์์ ๋ณด์ด๊ฒ ํ๋ค.

  ```css
  @supports ((-webkit-mask-image: url()) or (mask-image: url())) {
    background-color: var(--color-primary);
    mask-image: url(../img/chevron-thin-right.svg);
    -webkit-mask-image: url(../img/chevron-thin-right.svg);
    mask-size: cover;
    -webkit-mask-size: cover;
  }
  ```

### ๐ box-sizing: content-box๋ border ๋๋ฌธ์ ๋ด๋ถ ํฌ๊ธฐ๊ฐ ์ค์ด๋๋ ๋ฌธ์ ๋ฅผ ํด๊ฒฐํ๋ค.

```css
border: 3px solid #fff; /* border ๊ฐ ๋๊ป๊ธฐ ๋๋ฌธ์ ๋ด๋ถ ํฌ๊ธฐ๊ฐ ์ค์ด๋ ๋ค.(border-box) */
box-sizing: content-box;
```

### ๐ ๋์์ธ ์ฌ์ฌ์ฉ์ฑ์ ๋์ฌ์ฃผ๋ ์์ฑ๋ค

```css
font-size: inherit;
border-bottom: 1px solid currentColor;
background-color: transparent;
```
