# SCSS @function Directive

The `@function` directive in SCSS allows developers to create reusable functions that return values. These functions can be used to perform calculations, manipulate values, and streamline stylesheet development.

## Syntax
```scss
@function function-name($parameter1, $parameter2, ...) {
  @return computed-value;
}
```

Functions in SCSS always return a value using the `@return` directive.

---

## 1. Creating a Simple Function

**Example:**
```scss
@function double($value) {
  @return $value * 2;
}

.box {
  width: double(50px);
}
```

### Compiled CSS:
```css
.box {
  width: 100px;
}
```

---

## 2. Using Multiple Parameters
Functions can accept multiple parameters for more complex calculations.

**Example:**
```scss
@function calculate-area($width, $height) {
  @return $width * $height;
}

.container {
  height: calculate-area(10px, 20px);
}
```

### Compiled CSS:
```css
.container {
  height: 200px;
}
```

---

## 3. Conditional Logic in Functions
SCSS functions can include conditional logic using `@if` and `@else`.

**Example:**
```scss
@function convert-to-percent($value) {
  @if $value > 1 {
    @return 100%;
  } @else {
    @return $value * 100%;
  }
}

.progress {
  width: convert-to-percent(0.5);
}
```

### Compiled CSS:
```css
.progress {
  width: 50%;
}
```

---

## 4. Function Usage in Mixins
SCSS functions work well within mixins for greater flexibility.

**Example:**
```scss
@function rem($px) {
  @return $px / 16px * 1rem;
}

@mixin text-size($size) {
  font-size: rem($size);
}

.text {
  @include text-size(32px);
}
```

### Compiled CSS:
```css
.text {
  font-size: 2rem;
}
```

---

## Conclusion
SCSS `@function` allows developers to write reusable, efficient, and scalable styles by performing calculations and returning values. It enhances maintainability and ensures consistency across stylesheets.

