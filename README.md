Structure
=========

Lightweight SCSS layout, positioning &amp; opinionated defaults.



##How to use included media queries

###Example
```scss
  .page{
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
