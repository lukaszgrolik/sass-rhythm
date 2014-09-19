# Sass-rhythm

Sass-rhythm is a [Sass](https://github.com/nex3/sass) based tool that simplifies composing a vertical rhythm.

### Requirements

Sass 3.2.0+

## Installation

### Bower:

- Terminal: `bower install sass-rhythm`
- SCSS: `@import 'path/to/bower_components/sass-rhythm/rhythm';`

### Vanilla Sass

- Copy `_rhythm.scss` into your project
- SCSS: `@import 'path/to/rhythm';`

## Getting started

1. Set a base typography:

   ```scss
   html {
     @include rhythm-init(18px, 1.5, 'golden section');
   }
   ```

2. Change a `font-size` and adjust a `line-height`:

   ```scss
   // increases paragraph's font-size by 2 levels regarding to the chosen scale
   // and automatically adjusts its line-height
   p {
      @include rhythm-text(2);
   }
   ```

3. Change border-widths, margins, heights etc. in respect of the previously initialized typography:

   ```scss
   // sets a "padding-left" property to "5 * current line-height"
   padding-left: rhythm(5);
   // or
   padding-left: 5 * $rhythm;

   ```

## Reference

### Variables

- `$rhythm` - returns the base line-height's value in pixels.

### Functions

#### rhythm

Returns the base line-height's value in pixels multiplied by *n*.

```
rhythm([n])
```

- `n`
  - **type** - number (unitless)
  - **default value** - *1*

### Mixins

#### rhythm-init

Should be included once, most optimally in the `html` selector.

```
rhythm-init(font-size, line-height, modular-scale);
```
- `font-size`
  - **type** - number (px)
  - **description** - base font-size
- `line-height`
  - **type** - number (unitless)
  - **description** - base line-height
- `modular-scale`
  - **type** - number (unitless) or string (see *Predefined scale names*)
  - **description** - modular-scale which font-size and line-height will be based on

#### rhythm-text

Increases (or decreases) selector's font-size regarding to the chosen scale and automatically adjusts line-height.

Can be used within any selector.

```
rhythm-text(font-size[, line-height])
```

- `font-size`
  - **type** - number (unitless)
  - **description** - indicates how very enlarged or shrunk the text should be
- `line-height`
  - **type** - string (*tight* or *loose*)
  - **default value** - *loose*
  - **description** - sometimes text with *tight* line-height looks better (e.g. headings with large font-size above regular paragraphs)

### Predefined scale names

```
minor second   - 15/16
major second   - 8/9
minor third    - 5/6
major third    - 4/5
perfect fourth - 3/4
aug. fourth or
dim. fifth     - 1/1.41421356237
perfect fifth  - 2/3
minor sixth    - 5/8
golden section - 1/1.618
major sixth    - 3/5
minor seventh  - 9/16
major seventh  - 8/15
octave         - 1/2
major tenth    - 2/5
major eleventh - 3/8
major twelfth  - 1/3
double octave  - 1/4
```

## License

Sass-rhythm is released under the MIT License.

Copyright 2013 [Łukasz Grolik](https://github.com/lukaszgrolik)

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.