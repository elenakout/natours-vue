[Gradient Text Effect](##gradienttexteffect)

[Skew a sectiont](##skewAsection)

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

---

## Skew A section

This will `skew` the hole section

```css
transform: skewY(-7deg);
```

To `unskew` the content of the section we use `direct-child` selector (`>`)

```scss
& > * {
  transform: skewY(7deg);
}
```

---

## Implement a full rotate on a card element

```scss
.card {
  background-color: orangered;
  height: 50rem;
  transition: all 0.5sec ease;
}
```

When we `hover` we rotate `180deg` across the `Y` axis

```scss
&:hover {
  transform: rotateY(180deg);
}
```

To make it to pop out we use `prespective`.

We define `prespective` to the parent element and then we use the `direct-child` selector

For `firefox` we use `-moz-perspective`

```scss
perspective: 150rem;
-moz-perspective: 150rem;
```

We make a `div` for the card side

> `<div class="card__side"></div>`

```scss
&__side {
  background-color: orangered;
  height: 50rem;
  color: #fff;
  font-size: 2rem;
  transition: all 0.5sec;
}
```

```scss
&:hover &__side {
  transform: rotateY(180deg);
}
```

We use a `modifier class` for each side

```html
<div class="card__side--front">
  Front Side
</div>

<div class="card__side--back">
  Back Side
</div>
```

```scss
&--frond {
  background-color: orangered;
}

&--back {
  background-color: green;
  transform: rotateY(180deg);
}
```

And the `scss`

```scss
&:hover &__side--front {
  transform: rotateY(180deg);
}
&:hover &__side--back {
  transform: rotateY(0);
}
```

To have the divs on top of eachother we use the `absolute` position on the `card__side` class

```scss
&__side {
  position: absolute;
  top: 0;
  left: 0;
}
```

Parent must have a `relative` position so

```scss
.card {
  position: relative;
}
```

now they try to take all the pace next to eachother so we give them a `width`

And we use a property to hide the back side

```scss
&__side {
  width: 100%;
  backface-visibility: hidden;
}
```

To fix the collapse from the `absolute` positioning we give the parent the same `height`

```scss
.card {
  height: 50rem;
}
```
