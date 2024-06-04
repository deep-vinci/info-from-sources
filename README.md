# info-from-sources

- [css-tricks](https://css-tricks.com/fun-viewport-units/)  : difference between % and vw is most similar to the difference between em and rem. A % length is relative to local context (containing element) width, while a vw length is relative to the full width of the browser window.

```css
html {
  font-size: 62.5%; // base to 10px
}

body {
  font-size: 2.1rem; // this is 21px
}
```
[kevin powell, Are you using the right CSS units?](https://www.youtube.com/watch?v=N5wpD9Ov_To)
- use `%` for max-width for width
- 1 `ch` = width of 'o' in any font, 45-70 ch is a good width
- for padding btns use `em` because the if you increase the padding the font size will grow with them
- for text margins use `em` as for headers it will be respectively more, giving good whitespaces etc
- for media queries, use `em` 
- for shadows, border etc use `px`

[popular font stack on css-tricks](https://css-tricks.com/snippets/css/system-font-stack/)

```html
body {
  font-family: system-ui, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
}
```

[background css shorthand formal syntax](https://developer.mozilla.org/en-US/docs/Web/CSS/background)

Sure, here's a more concise and easier-to-read syntax for the `background` property in CSS:

```
background: <bg-layer> [, <bg-layer>]* [, <final-bg-layer>]?;

<bg-layer> =
  <bg-image> |
  <position> / <bg-size>? |
  <repeat-style> |
  <attachment> |
  <box> <box>?;

<final-bg-layer> =
  <bg-image> |
  <position> / <bg-size>? |
  <repeat-style> |
  <attachment> |
  <box> <box>? |
  <bg-color>;

<bg-image> = <url> | <gradient> | none;
<position> = [left|center|right|<length>] [top|center|bottom|<length>];
<bg-size> = <length> <length>? | cover | contain;
<repeat-style> = repeat-x | repeat-y | [repeat|space|round|no-repeat]{1,2};
<attachment> = scroll | fixed | local;
<box> = border-box | padding-box | content-box;
<bg-color> = <color>;
```

In this syntax:

- `background` is a shorthand property that accepts one or more `<bg-layer>` values, optionally followed by a `<final-bg-layer>`.
- `<bg-layer>` can be a `<bg-image>`, `<position> / <bg-size>?`, `<repeat-style>`, `<attachment>`, or a combination of two `<box>` values.
- `<final-bg-layer>` can be any of the values allowed for `<bg-layer>`, plus a `<bg-color>`.
- `<bg-image>` can be a URL, gradient, or the keyword `none`.
- `<position>` defines the background image's position with keyword values or lengths.
- `<bg-size>` sets the background image's size with lengths or the keywords `cover` or `contain`.
- `<repeat-style>` defines how the background image repeats.
- `<attachment>` determines if the background image scrolls or is fixed.
- `<box>` specifies which box area the background should be clipped to.
- `<bg-color>` sets the background color.

This syntax is more compact and easier to read, while still capturing the essential structure and valid values for the `background` property.


### entire syntax is being followed 
```css
//          bg-img             position / bg-size    repeat-style attachment box box
background: url("pattern.png") 20px 30px/100px 200px repeat-x fixed padding-box content-box, 
            linear-gradient(to bottom, #fff, #ccc) center/cover no-repeat border-box,
            #f0f0f0;
```
