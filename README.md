# universal-checklist

1. [CODE STYLE] - Add empty lines between multiline sibling blocks of HTML.
But don't add empty lines between parent and child elements

GOOD example:
```html
<ul>
  <li class="nav__item">
    <a href="#home">Home</a>
  </li>

  <li class="nav__item">
    <a href="#shop">Shop</a>
  </li>

  <li class="nav__item">
    <a href="#contacts">Contacts</a>
  </li>
</ul>
```
BAD example:
```html
<ul>

  <li class="nav__item">
    <a href="#home">Home</a>
  </li>
  <li class="nav__item">
    <a href="#shop">Shop</a>
  </li>
  <li class="nav__item">
    <a href="#contacts">Contacts</a>
  </li>

</ul>
```

2. [CODE STYLE] - If several selectors MUST always have the same styles, group them using `,` to prevent accidental out ot sync in future

GOOD example:
```css
.block--1,
.block--2,
.block--3 {
  background-color: yellowgreen;
}
```

BAD example:
```css
.block--1 {
  background-color: yellowgreen;
}

.block--2 {
  background-color: yellowgreen;
}

.block--3 {
  background-color: yellowgreen;
}
```

3. [STYLE] - Don't set fixed container size. Let the content size dictate it.


4. [CODE STYLE] - Remember about correct indentation between parent and child
elements. Each level of nesting, including text, contained inside the element,
requires 2-space offset.
        <details>
          <summary>BAD examples</summary>
            ![html-indentations-bad-example-1](https://mate-academy.github.io/fe-program/css/checklists/html-indentations/example-bad-1.png)
        </details>
        <details>
          <summary>GOOD example</summary>
            ![html-indentations-good-example-1](https://mate-academy.github.io/fe-program/css/checklists/html-indentations/example-good-1.png)
        </details>



5. [CODE STYLE] - If the HTML-element has long attribute values or number of
attributes is more than 2 - start each one, including the first, on the new
line with 2-space indentation related to tag. Tag’s closing bracket should be
on the same level as opening one.
        <details>
          <summary>BAD examples</summary>
            ![html-attributes-bad-example-1](https://mate-academy.github.io/fe-program/css/checklists/html-attributes/example-bad-1.png)
            ![html-attributes-bad-example-2](https://mate-academy.github.io/fe-program/css/checklists/html-attributes/example-bad-2.png)
            ![html-attributes-bad-example-3](https://mate-academy.github.io/fe-program/css/checklists/html-attributes/example-bad-3.png)
            ![html-attributes-bad-example-4](https://mate-academy.github.io/fe-program/css/checklists/html-attributes/example-bad-4.png)
        </details>
        <details>
          <summary>GOOD example</summary>
            ![html-attributes-good-example-1](https://mate-academy.github.io/fe-program/css/checklists/html-attributes/example-good-1.png)
        </details>


6. [FUNCTIONAL] - You need to use a label tag for each input, so that every
input could be activated by clicking on the corresponding label.


7. [STYLES] - if you have two or more similar elements with portions of similar styles with different values - use one
of the elements as the basic case, and override necessary styles for other cases.
Explanation: The point is not in the names of the classes, the point is: when there are several similar elements, ex., 2 inputs, for one we can give a class `input`, for example, and for the second - `input input--small`. We write all the styles for `.input`, but for `.input-small` we write only those styles that differ in design, and we need this second input to look a little different.
Element with class `.input` without extra classes should also look like a full-fledged styled element.
       <details>
         <summary>BAD example</summary>
           ![css-variations-bad-example-html-1](https://mate-academy.github.io/fe-program/css/checklists/css-variations/example-bad-html-1.png)
           ![css-variations-bad-example-css-1](https://mate-academy.github.io/fe-program/css/checklists/css-variations/example-bad-css-1.png)
       </details>
       <details>
         <summary>GOOD example</summary>
           ![css-variations-good-example-html-1](https://mate-academy.github.io/fe-program/css/checklists/css-variations/example-good-html-1.png)
           ![css-variations-good-example-css-1](https://mate-academy.github.io/fe-program/css/checklists/css-variations/example-good-css-1.png)
       </details>


8. [STYLES] - Remember to use fallback fonts - alternative font-family in case the main one doesn't work [like this](https://www.w3schools.com/cssref/pr_font_font-family.asp)


9. [CODE STYLE] - Remember about correct indentation between parent and child
elements. Each level of nesting, including text, contained inside the element,
requires 2-space offset. Also blank line shouldn't be between parent and child elements.
       <details>
         <summary>BAD examples</summary>
           ![html-indentations-bad-example-1](https://mate-academy.github.io/fe-program/css/checklists/html-indentations/example-bad-1.png)
       </details>
       <details>
         <summary>GOOD example</summary>
           ![html-indentations-good-example-1](https://mate-academy.github.io/fe-program/css/checklists/html-indentations/example-good-1.png)
       </details>


10. [CODE KNOWLEDGE] - Don't use `*` selector for zeroing out your margins or paddings. It's still inefficient for browser to read your web document


11. [STYLES] - Don't hardcode exact height size. Add necessary paddings according to mockup
and let content dictate the container size.



12. [STYLES] - Don't add new border to the element on hover. Add default
transparent border of the same width, and change its color on `:hover`


13. [BEM & STYLES] - Don't add external styles (positioning or margins) to
   BEM-blocks. Use mix where necessary and move all external styles under element
   selector.

GOOD example
```html
<!--index.html-->
<div class="container">
  <div class="container__card card">
    ...
  </div>
</div>
```
```css
/*style.css*/
.container__card {
  margin: 48px 24px;
}

.card {
  font-size: 16px;
  background-color: purple;
}
```

BAD example
```html
<!--index.html-->
<div class="container">
  <div class="card">
    ...
  </div>
</div>
```
```css
/*style.css*/
.card {
  margin: 48px 24px;
  font-size: 16px;
  background-color: purple;
}
```


14. [SASS] - use variables for the main values so that you'll be able to reuse
    them and give them descriptive names. But don't overuse them, don't create
    variable for the value that's used just once.
15. [SASS] - Try to use different features - mixins etc - where it makes sense.
16. [CODE STYLE] - Remember about styles properties order - ([css order](https://codeguide.academy/html-css.html#css-order))
17. [CODE KNOWLEDGE] - Make sure to add transition style under general selector, not the one with :hover - this way transition will work smoothly both ways.

