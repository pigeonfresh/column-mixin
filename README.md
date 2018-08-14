# Column mixin
This mixin can be used when you have to serve a layout with columns and a fixed gutter between these columns. The
This column mixin can be used to calculate the max-width of a block. The mixin as it is setup now has 12 columns with a gap of 40px between the gutters. If you had to have a div spread across 3 columns you could use the column mixin to return a calculation.

```css
.container {
    @include column(3); // max-width: calc(25% - 30px);
}
```

If you had to spread 3 columns in a wrapper that already had a columns value assigned to it you can add a second parameter.

```css
.wrapper {
    @include column(6); // max-width: calc(50% - 20px);

    .container {
        @include column(3, 6); // max-width: calc(50% - 20px);
    }
}
```

[Codepen Example](https://codepen.io/pigeonfresh/pen/MBRvLL)