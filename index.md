---
layout: default
title: Your New Jekyll Site
---

<div id="home">
  <h1>Blog Posts</h1>
  <ul class="posts">
    {% for post in site.posts %}
      <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
</div>

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

