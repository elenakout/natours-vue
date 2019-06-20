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
