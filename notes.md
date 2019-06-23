[Gradient Text Effect](##gradienttexteffect)

## Gradient Text Effect

Set a `backgrount-image` to the `<h#>` with a `linear-gradient`

```css
background-image: linear-gradient(
  to right,
  $color-primary-light,
  $color-primary-dark
);
```

We want the `background-color` to be only behind the text and stop when the text stop.

Because `<h#>` is a `block` element we need to change it to `inline-block`

```scss
display: inline-block;
```

For the effect to be only on the text we use `-webkit-background-clip`

This will clip the background only to where the text is

```css
-webkit-background-clip: text;
```

And now we have the `background-image` hidden behind the text

so we make the text `transparent` so we can see the background

```css
color: transparent;
```

---

## Moving Text on Hover

We use the `transform` property

We can put multiple things we want to transform

> `skewY(degrees)`
>
> `skewX(degrees)`
>
> `scale(percent)`

```scss
&:hover {
  transform: skewY(2deg) skewX(15deg) scale(1.1);
}
```

We put the `transform` property to the element we want

```css
.heading {
  transition: all 0.2s;
}
```

---

## Utility Classes

Utility classes are very simple classes which only hane one goal

```css
.u-center-text {
  text-align: center;
}

.u-margin-bottom-8 {
  margin-bottom: 8rem;
}
```

---

## FontAwsome

```html
<link
  rel="stylesheet"
  href="https://use.fontawesome.com/releases/v5.2.0/css/all.css"
  integrity="sha384-hWVjflwFxL6sNzntih27bfxkr27PmbbK/iSvJ+a4+0owXq79v+lsFkW54bOGbiDQ"
  crossorigin="anonymous"
/>
```

```css
<i class="fas fa-globe"></i>
```
