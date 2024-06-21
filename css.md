## Stacking context

stacking context is basically grouping layers, there are many many properties which affects the layers isolation 

```css
isolation: isolate;
``` 
is recommended way to create groupings

https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_positioned_layout/Understanding_z-index/Stacking_context


## Media queries

```css
@media (max-width: 500px) {}
@media (width <= 1250px) {
@media screen and (max-width: 500px) { //for screen }
@media print { //for print }
```

`max-width` query will apply on any screen up to the defined max-width
`min-width` query will apply on any screen larger than the defined min-width 

[a refresher on min and Max width](https://www.shecodes.io/athena/133814-what-is-min-width-and-max-width-in-css)