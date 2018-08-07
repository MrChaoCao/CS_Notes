# Media Query
Media query is a css property that has only executes if a certain condition is true. This lets you check what the state of the user's browser is and adjust your display accordingly.

```
@media only screen and (max-width: 600px) {
    body {
        background-color: lightblue;
    }
}
```

## Break point
Defined window sizes where your display properties change. Use in conjunction with Media Query to make a site responsive.

## Mobile first
Don't start at full size and then adjust smaller. Design small and then adjust for bigger. This will be less of a burden on smaller devices.

## Portrait / landscape
You can set the display based on the orientation of the browser.

## Hiding elements
You can hide elements based on the size of the browser.

```
@media only screen and (max-width: 600px) {
  div.example {
    display: none;
  }
}
```
