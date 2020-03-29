# `place-items`: A shorthand to set values for `align-items` and `justify-items`
Instead of writing:
```css
.container {
  justify-items: center;
  align-items: flex-end;
}
```
We can utilise `place-items` to set values for both `align-items` and `justify-items`.
```css
.container {
  /* place-items: <align-items> <justify-items> */
  place-items: flex-end center;
}
```
If we wish to have the same value for both `align-items` and `justify-items`, we can set `place-items` to just one value.
```css
.container {
  place-items: center;
}
```
