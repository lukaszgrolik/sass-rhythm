# Rhythm

Rhythm is a [Sass](https://github.com/nex3/sass)-based tool that simplifies composing a vertical rhythm.

### Requirements

Sass 3.2.0+

### Browser support

Rhythm should work in every non-text browser.

## Getting started

1. Download & put the `_rhythm.scss` partial wherever you want in your project
2. Import:

   ```scss
   @import 'path/to/rhythm';
   ```

3. Set a base typography:

   ```scss
   @include rhythm-init(18px, 1.5, 'golden section');
   ```

4. Change a `font-size` & adjust a `line-height`:
  
   ```scss
   // increases a font-size by 2 levels regarding to the chosen scale
   // and automatically adjusts a line-height
   @include rhythm-text(2);
   ```

5. Change paddings, border-widths & margins, width, heights etc. in respect of the previously initialized typography:

   ```scss
   // sets a "padding-left" property to "5 * current line-height"
   padding-left: rhythm(5);
   ```

## License

Respond is released under the MIT License.

Copyright 2013 [Łukasz Grolik](http://lukaszgrolik.pl)

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