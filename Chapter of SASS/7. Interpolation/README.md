# SCSS Interpolation

SCSS Interpolation allows dynamic insertion of variables, expressions, and other values within selectors, properties, and values using `#{}` syntax. It makes stylesheets more flexible and maintainable.

## Syntax
The interpolation syntax in SCSS is:
```scss
#{expression}
```
This allows embedding variables, functions, and expressions in places where normal variable usage is not allowed.

---

## 1. Interpolation in Selectors
Interpolation can be used to dynamically create selectors.

**Example:**
```scss
$btn-name: "primary";

.btn-#{ $btn-name } {
  background-color: blue;
  color: white;
}
```

### Compiled CSS:
```css
.btn-primary {
  background-color: blue;
  color: white;
}
```

---

## 2. Interpolation in Property Names
You can use interpolation to dynamically set property names.

**Example:**
```scss
$property: "margin";
$size: 10px;

.box {
  #{ $property }-top: $size;
}
```

### Compiled CSS:
```css
.box {
  margin-top: 10px;
}
```

---

## 3. Interpolation in Property Values
Interpolation is useful for constructing dynamic property values.

**Example:**
```scss
$base-color: red;
$opacity: 0.5;

.alert {
  background-color: #{ $base-color };
  opacity: #{ $opacity };
}
```

### Compiled CSS:
```css
.alert {
  background-color: red;
  opacity: 0.5;
}
```

---

## 4. Interpolation in @import and @media Queries
Interpolation can also be used in `@import` and `@media` directives.

**Example:**
```scss
$breakpoint: 768px;

@media (max-width: #{ $breakpoint }) {
  .responsive {
    display: none;
  }
}
```

### Compiled CSS:
```css
@media (max-width: 768px) {
  .responsive {
    display: none;
  }
}
```

---

## Conclusion
SCSS Interpolation is a powerful feature that enhances flexibility in writing dynamic styles. It allows embedding variables and expressions in selectors, property names, property values, and directives efficiently.

