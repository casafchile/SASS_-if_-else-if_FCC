Use @if and @else to Add Logic To Your Styles


The @if directive in Sass is useful to test for a specific case - it works just like the if statement in JavaScript.

    @mixin make-bold($bool) {
      @if $bool == true {
        font-weight: bold;
      }
    }
And just like in JavaScript, the @else if and @else directives test for more conditions:

    @mixin text-effect($val) {
      @if $val == danger {
        color: red;
      }
      @else if $val == alert {
        color: yellow;
      }
      @else if $val == success {
        color: green;
      }
      @else {
        color: black;
      }
    }
Create a mixin called border-stroke that takes a parameter $val. The mixin should check for the following conditions using @if, @else if, and @else directives:

    light - 1px solid black
    medium - 3px solid black
    heavy - 6px solid black
If the $val parameter value is not light, medium, or heavy, then the border property should be set to none.
