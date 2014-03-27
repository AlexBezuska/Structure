Structure
=========

Lightweight SCSS layout, positioning &amp; opinionated defaults.



##How to use included media queries

###Example
```scss
  .page{
    @include bp(papa-bear) {
      width: 80%;
    }

    @include bp(mama-bear) {
      width: 50%;
    }

    @include bp(baby-bear) {
      min-width: 370px;
      max-width: 100%;
    }
  }
```