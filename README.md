# CSS-tips

Using ems can be convenient when setting properties like padding, height, width,
or border-radius


use rems for font sizes, pixels for borders, and ems for most other measures,
especially paddings, margins, and border radius

```
*,
::before,
::after {
box-sizing: border-box;
}
```

More robust universal border-box fix
third-party components with their own CSS might break if they are not using border-box 

```
:root {
box-sizing: border-box;
}
*,
::before,
::after {

box-sizing: inherit;
}

.third-party-component {
box-sizing: content-box;
}
```

