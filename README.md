Structure
=========

Lightweight SCSS layout, positioning system based on [Chris Coyier's](https://github.com/chriscoyier/) Don't Overthink It Grids. [Read his article](http://css-tricks.com/dont-overthink-it-grids/)

---

###Column layouts

Layouts in structure are based on rows and columns, columns do not have to be inside rows, but you will get much more predictable results if they are.
Everything in Structure is centered around fractions, and all of the fractions are created using pre-defined percents. You can use any comination of two numbers from 1 to 10 to create your fractions, here is an example:

####Half and half columns
```html
<div class='row'>
    <div class='col1-2'>
        I take up 1/2 of the total width of this row.
    </div>
    <div class='col1-2'>
         I take up 1/2 of the total width of this row.
    </div>
</div>
```
####Thirds columns
```html
<div class='row'>
    <div class='col1-3'>
        I take up 1/3 of the total width of this row.
    </div>
    <div class='col1-3'>
         I take up 1/3 of the total width of this row.
    </div>
      <div class='col1-3'>
         I take up 1/3 of the total width of this row.
    </div>
</div>
```

####Mix & Match
```html
<div class='row'>
    <div class='col1-2'>
        I take up 1/2 of the total width of this row.
    </div>
    <div class='col1-4'>
         I take up 1/4 of the total width of this row.
    </div>
      <div class='col1-4'>
         I take up 1/4 of the total width of this row.
    </div>
</div>
```

####Go crazy!
```html
<div class='row'>
    <div class='col5-10'>
        I take up 1/2 of the total width of this row.
    </div>
    <div class='col2-10'>
         I take up 1/4 of the total width of this row.
    </div>
      <div class='col3-10'>
         I take up 1/4 of the total width of this row.
    </div>
</div>
```

---

###How to use included media queries
Basically there cover 'desktop', 'tablet', and 'phone', the reason they are all in quotes is because the lines between these devices are becoming more and more blurred all the time.

###Example Usage
```scss
  .page{
    position: relative;
    background: white;
    
    @include breakpoint(papa-bear) {
      width: 80%;
    }

    @include breakpoint(mama-bear) {
      width: 50%;
    }

    @include breakpoint(baby-bear) {
      min-width: 370px;
      max-width: 100%;
    }
    
  }
```


You can adjust the pixel width ranges of the media queries in the _structure.scss file here:

```scss
@mixin breakpoint($point) {
  @if $point == papa-bear {
    @media (min-width: 1025px)  { 
      @content; 
    }
  }
  @else if $point == mama-bear {
    @media (min-width: 731px) and (max-width: 1024px) { 
      @content; 
    }
  }
  @else if $point == baby-bear {
    @media (min-width: 320px) and (max-width: 730px)  { 
      @content; 
    }
  }
}
```
Structure is set to these resonable defaults:

#####Papa Bear
1025px +

#####Mama Bear
731px - 1024px


#####Baby Bear
320px - 730px
