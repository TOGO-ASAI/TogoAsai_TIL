## Flex
|Propaty |	Behavior |
| --- | --- |
| flex: 1 | Expands to fill available space |
| flex: 0 1 auto |	Default (shrinks if necessary)　|
| flex: none |	Neither grows nor shrinks; size stays fixed　|

```html
<div class="container">
  <div class="box A">A</div>
  <div class="box B">B</div>
</div>
```

```css
.container {
  display: flex;
  width: 180px;
}

.box {
  width: 100px;
}

.B {
  flex: none;
}
```

In the above code, box A gets to be shrinked because `flex-shrink:1;` will work for the code. On the other hand, the width of box B is fixed to 100px because of `flex: none;`.
