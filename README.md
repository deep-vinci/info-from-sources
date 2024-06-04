# info-from-sources

- (css-tricks)[https://css-tricks.com/fun-viewport-units/]  : difference between % and vw is most similar to the difference between em and rem. A % length is relative to local context (containing element) width, while a vw length is relative to the full width of the browser window.

```css
html {
  font-size: 62.5%; // base to 10px
}

body {
  font-size: 2.1rem; // this is 21px
}
```
(kevin powell, Are you using the right CSS units?)[https://www.youtube.com/watch?v=N5wpD9Ov_To]
use `%` for max-width for width
1 `ch` = width of 'o' in any font, 45-70 ch is a good width
for padding btns use `em` because the if you increase the padding the font size will grow with them
for text margins use `em` as for headers it will be respectively more, giving good whitespaces etc
for media queries, use `em` 
for shadows, border etc use `px`
