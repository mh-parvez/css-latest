# SCSS Operators

SCSS provides several types of operators to perform calculations and manipulations in stylesheets. These operators help to create dynamic and reusable styles. The five types of operators in SCSS are:

1. **Arithmetic Operators**
2. **Relational Operators**
3. **Equality Operators**
4. **Logical Operators**
5. **String Operators**

## 1. Arithmetic Operators
These operators allow you to perform mathematical calculations on numbers, colors, and variables.

**Operators:** `+` (addition), `-` (subtraction), `*` (multiplication), `/` (division), `%` (modulus)

**Example:**
```scss
$width: 100px;
$height: $width / 2;

.box {
  width: $width + 50px;
  height: $height;
}
```

### Compiled CSS:
```css
.box {
  width: 150px;
  height: 50px;
}
```

---

## 2. Relational Operators
Used for comparing values and returning `true` or `false`.

**Operators:** `<`, `>`, `<=`, `>=`

**Example:**
```scss
$size: 30px;

@if $size > 20px {
  .large-text {
    font-size: $size;
  }
}
```

### Compiled CSS:
```css
.large-text {
  font-size: 30px;
}
```

---

## 3. Equality Operators
These operators compare values and return a boolean result.

**Operators:** `==`, `!=`

**Example:**
```scss
$theme: light;

@if $theme == light {
  .theme {
    background-color: white;
    color: black;
  }
} @else {
  .theme {
    background-color: black;
    color: white;
  }
}
```

### Compiled CSS:
```css
.theme {
  background-color: white;
  color: black;
}
```

---

## 4. Logical Operators
These operators are used for conditional logic.

**Operators:** `and`, `or`, `not`

**Example:**
```scss
$primary: true;
$secondary: false;

@if $primary and not $secondary {
  .btn {
    background-color: blue;
    color: white;
  }
}
```

### Compiled CSS:
```css
.btn {
  background-color: blue;
  color: white;
}
```

---

## 5. String Operators
Used for manipulating strings.

**Operators:** `+` (concatenation)

**Example:**
```scss
$base: ".btn";
$modifier: "-primary";

#{ $base + $modifier } {
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

## Conclusion
SCSS operators make it easier to handle calculations, comparisons, and conditions in stylesheets. By using these operators effectively, you can create more dynamic and maintainable styles.

