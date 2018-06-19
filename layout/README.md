# Layout On Mobile

## Function

To be adaptive with different resolution mobile.

- Adaptive with different DPR mobile not only with DPR=2.
- Implement the smallest border on high resolution mobile.
- Minimize the impact of decimals.

## Usage

- Put the code below in the `head` and make it execute as early as possible.

```html
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <script>
    //inline script in demo.html
  </script>
```

- Use `rem` instead of `em` or `px` when setting the `font-size`.
- Use `vw` when setting the `width`, `height` of element.
- Use `vw` when setting the `border` with value which is bigger than 1px.
- Use `1px` when setting the `border` with value = 1px.
- Had better leave the `margin` to browser instead of setting it with numbers.

## Principle

- Make the `font-size` connect with DPR by `rem`.
- Use viewport scale to solve the problem of 1px on `border` and `font-size`.
- Make the width and height of element connect with device-width by `vw`.
- Leave the decimals to browser by `flex`.

## Hint

- Sometimes decimals might bother you. At that moment you may try to leave the decimals to browser by using `flex`, `margin:auto` or other flexible property.

- I didn't handle the problem of `img` on retina screen. You might seek some help from [retina.js][retina.js].

[retina.js]: https://github.com/strues/retinajs
