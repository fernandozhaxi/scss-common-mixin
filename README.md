# scss-common-mixins

Scss mixins often used.

## Content Table

- [Install](#install)
- [Import](#import)
- [Examples](#examples)
  - [background-gradient](#background-gradient)
  - [background-gradient-x](#background-gradient-x)
  - [background-gradient-y](#background-gradient-y)
  - [background-cover](#background-cover)
  - [background-contain](#background-contain)
  - [border-top-radius](#border-top-radius)
  - [border-right-radius](#border-right-radius)
  - [border-bottom-radius](#border-bottom-radius)
  - [border-left-radius](#border-left-radius)
  - [caret-up](#caret-up)
  - [caret-right](#caret-right)
  - [caret-down](#caret-down)
  - [caret-left](#caret-left)
  - [circle](#circle)
  - [clearfix](#clearfix)
  - [flex-center](#flex-center)
  - [hr](#hr)
  - [list-unstyle](#list-unstyle)
  - [rect](#rect)
  - [square](#square)
  - [text-truncate](#text-truncate)

## Install

```sh
npm install --save scss-common-mixins
```

## Import

```scss
@import 'node_modules/scss-common-mixins/index.scss';
```

## Examples

### background-gradient

**Usage:**

```scss
@include background-gradient($begin, $end, $angle: 180deg);
```

**Input:**

```scss
.background-gradient-default {
  @include background-gradient(#fff, #000);
}

.background-gradient-custom-angle {
  @include background-gradient(#fff, #000, 60deg);
}
```

**Output:**

```css
.background-gradient-default {
  background-color: #808080;
  background-image: linear-gradient(180deg, #fff, #000);
}

.background-gradient-custom-angle {
  background-color: #808080;
  background-image: linear-gradient(60deg, #fff, #000);
}
```

### background-gradient-x

**Usage:**

```scss
@include background-gradient-x($begin, $end);
```

**Input:**

```scss
.background-gradient-x {
  @include background-gradient-x(#fff, #000);
}
```

**Output:**

```css
.background-gradient-x {
  background-color: #808080;
  background-image: linear-gradient(90deg, #fff, #000);
}
```

### background-gradient-y

**Usage:**

```scss
@include background-gradient-y($begin, $end);
```

**Input:**

```scss
.background-gradient-y {
  @include background-gradient-y(#fff, #000);
}
```

**Output:**

```css
.background-gradient-y {
  background-color: #808080;
  background-image: linear-gradient(180deg, #fff, #000);
}
```

### background-cover

**Usage:**

```scss
@include background-cover($image);
```

**Input:**

```scss
.background-cover {
  @include background-cover('url(image)');
}
```

**Output:**

```css
.background-cover {
  background-image: 'url(image)';
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}
```

### background-contain

**Usage:**

```scss
@include background-contain($image);
```

**Input:**

```scss
.background-contain {
  @include background-contain('url(image)');
}
```

**Output:**

```css
.background-contain {
  background-image: 'url(image)';
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
}
```

### border-top-radius

**Usage:**

```scss
@include border-top-radius($radius);
```

**Input:**

```scss
.border-top-radius {
  @include border-top-radius(10px);
}
```

**Output:**

```css
.border-top-radius {
  border-top-right-radius: 10px;
  border-top-left-radius: 10px;
}
```

### border-right-radius

**Usage:**

```scss
@include border-right-radius($radius);
```

**Input:**

```scss
.border-right-radius {
  @include border-right-radius(10px);
}
```

**Output:**

```css
.border-right-radius {
  border-top-right-radius: 10px;
  border-botton-right-radius: 10px;
}
```

### border-bottom-radius

**Usage:**

```scss
@include border-bottom-radius($radius);
```

**Input:**

```scss
.border-bottom-radius {
  @include border-bottom-radius(10px);
}
```

**Output:**

```css
.border-bottom-radius {
  border-bottom-right-radius: 10px;
  border-bottom-left-radius: 10px;
}
```

### border-left-radius

**Usage:**

```scss
@include border-left-radius($radius);
```

**Input:**

```scss
.border-left-radius {
  @include border-left-radius(10px);
}
```

**Output:**

```css
.border-left-radius {
  border-top-left-radius: 10px;
  border-botton-left-radius: 10px;
}
```

### caret-up

**Usage:**

```scss
@include caret-up($size, $color);
```

**Input:**

```scss
.caret-up-default {
  @include caret-up();
}

.caret-up-custom {
  @include caret-up(12px, #000);
}
```

**Output:**

```css
.caret-up-default {
  border-top: 0;
  border-right: 8px solid transparent;
  border-bottom: 8px solid #666;
  border-left: 8px solid transparent;
}

.caret-up-custom {
  border-top: 0;
  border-right: 12px solid transparent;
  border-bottom: 12px solid #000;
  border-left: 12px solid transparent;
}
```

### caret-right

**Usage:**

```scss
@include caret-right($size, $color);
```

**Input:**

```scss
.caret-right-default {
  @include caret-right();
}

.caret-right-custom {
  @include caret-right(12px, #000);
}
```

**Output:**

```css
.caret-right-default {
  border-top: 8px solid transparent;
  border-right: 0;
  border-bottom: 8px solid transparent;
  border-left: 8px solid #666;
}

.caret-right-custom {
  border-top: 12px solid transparent;
  border-right: 0;
  border-bottom: 12px solid transparent;
  border-left: 12px solid #000;
}
```

### caret-down

**Usage:**

```scss
@include caret-down($size, $color);
```

**Input:**

```scss
.caret-down-default {
  @include caret-down();
}

.caret-down-custom {
  @include caret-down(12px, #000);
}
```

**Output:**

```css
.caret-down-default {
  border-top: 8px solid #666;
  border-right: 8px solid transparent;
  border-bottom: 0;
  border-left: 8px solid transparent;
}

.caret-down-custom {
  border-top: 12px solid #000;
  border-right: 12px solid transparent;
  border-bottom: 0;
  border-left: 12px solid transparent;
}
```

### caret-left

**Usage:**

```scss
@include caret-left($size, $color);
```

**Input:**

```scss
.caret-left-default {
  @include caret-left();
}

.caret-left-custom {
  @include caret-left(12px, #000);
}
```

**Output:**

```css
.caret-left-default {
  border-top: 8px solid transparent;
  border-right: 8px solid #666;
  border-bottom: 8px solid transparent;
  border-left: 0;
}

.caret-left-custom {
  border-top: 12px solid transparent;
  border-right: 12px solid #000;
  border-bottom: 12px solid transparent;
  border-left: 0;
}
```

### circle

**Usage:**

```scss
@include circle($size);
```

**Input:**

```scss
.circle {
  @include circle(20px);
}
```

**Output:**

```css
.circle {
  width: 20px;
  height: 20px;
  border-radius: 50%;
}
```

### clearfix

**Usage:**

```scss
@include clearfix();
```

**Input:**

```scss
.clearfix {
  @include clearfix();
}
```

**Output:**

```css
.clearfix:after {
  display: table;
  clear: both;
  content: "";
}
```

### flex-center

**Usage:**

```scss
@include flex-center();
```

**Input:**

```scss
.flex-center {
  @include flex-center();
}
```

**Output:**

```css
.flex-center {
  display: flex;
  align-items: center;
  justify-content: center;
}
```

### hr

**Usage:**

```scss
@include hr($color, $size: 1px, $style: solid, $direction: horizontal);
```

**Input:**

```scss
.hr-default {
  @include hr(#eee);
}

.hr-custom {
  @include hr(#eee, 2px, dashed, vertical);
}
```

**Output:**

```css
.hr-default {
  width: 100%;
  border-top: 1px solid #eee;
}
.hr-custom {
  height: 100%;
  border-left: 2px dashed #eee;
}
```

### list-unstyle

**Usage:**

```scss
@include list-unstyle();
```

**Input:**

```scss
.list-unstyle {
  @include list-unstyle();
}
```

**Output:**

```css
.list-unstyle {
  padding-left: 0;
  list-style: none;
}
```

### rect

**Usage:**

```scss
@include rect($width, $height);
```

**Input:**

```scss
.rect {
  @include rect(10px, 20px);
}
```

**Output:**

```css
.rect {
  width: 10px;
  height: 20px;
}
```

### square

**Usage:**

```scss
@include square($size);
```

**Input:**

```scss
.square {
  @include square(10px);
}
```

**Output:**

```css
.square {
  width: 10px;
  height: 10px;
}
```

### text-truncate

**Usage:**

```scss
@include text-truncate($rows: 1);
```

**Input:**

```scss
.text-truncate-default {
  @include text-truncate();
}

.text-truncate-custom {
  @include text-truncate(3);
}
```

**Output:**

```css
.text-truncate-default {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

.text-truncate-custom {
  display: -webkit-box;
  overflow: hidden;
  text-overflow: ellipsis;
  word-break: break-all;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 3;
}
```

## License

MIT.
