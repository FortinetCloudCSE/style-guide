---
title: "Ch 1 - Markdown"
chapter: True
menuTitle: "Markdown"
weight: 35
---

#### Where do I begin?

##### H5

###### H6

When typing things, theres **bold text**, _italicized text_, ~~strike through~~, 

Double quotes `"` and single quotes `'` of enclosed text are replaced by **"double curly quotes"** and **'single curly quotes'**.

Double dashes `--` and triple dashes `---` are replaced by en-dash **--** and em-dash **---** entities.

Double arrows pointing left `<<` or right `>>` are replaced by arrow **<<** and **>>** entities.

Three consecutive dots `...` are replaced by an ellipsis **...** entity.

---

- Lorem ipsum dolor sit amet
- Consectetur adipiscing elit
  - Vestibulum laoreet porttitor sem
  - Ac tristique libero volutpat at
- Nulla volutpat aliquam velit
  - Phasellus iaculis neque
  - Purus sodales ultricies
- Faucibus porta lacus fringilla vel

---

1. Lorem ipsum dolor sit amet
3. Consectetur adipiscing elit
    1. Integer molestie lorem at massa
    7. Facilisis in pretium nisl aliquet
99. Nulla volutpat aliquam velit
    1. Faucibus porta lacus fringilla vel
    1. Aenean sit amet erat nunc
17. Eget porttitor lorem

---

- [x] Basic Test
- [ ] More Tests
  - [x] View
  - [x] Hear
  - [ ] Smell

  ---

Apple
: Pomaceous fruit of plants of the genus Malus in the family Rosaceae.
: An American computer company.

Orange
: The fruit of an evergreen tree of the genus Citrus.

  You can make juice out of it.
: A telecommunication company.

  You can't make juice out of it.

---

In this example, `<div></div>` is marked as code.

---

Be impressed by my advanced code:

    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code

---

```js
grunt.initConfig({
  assemble: {
    options: {
      assets: 'docs/assets',
      data: 'src/data/*.{json,yml}',
      helpers: 'src/custom-helpers.js',
      partials: ['src/partials/**/*.{hbs,md}']
    },
    pages: {
      options: {
        layout: 'default.hbs'
      },
      files: {
        './': ['src/templates/pages/index.hbs']
      }
    }
  }
};
```

---

Tables

| Option | Description |
|--------|-------------|
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |

---

Aligned Columns

| Option | Number | Description |
|-------:|:------:|:------------|
| data   | 1      | path to data files to supply the data that will be passed into templates. |
| engine | 2      | engine to be used for processing templates. Handlebars is the default. |
| ext    | 3      | extension to be used for dest files. |

---

> Donec massa lacus, ultricies a ullamcorper in, fermentum sed augue. Nunc augue augue, aliquam non hendrerit ac, commodo vel nisi.
>
> > Sed adipiscing elit vitae augue consectetur a gravida nunc vehicula. Donec auctor odio non est accumsan facilisis. Aliquam id turpis in dolor tincidunt mollis ac eu diam.
>
> Mauris sit amet ligula egestas, feugiat metus tincidunt, luctus libero. Donec congue finibus tempor. Vestibulum aliquet sollicitudin erat, ut aliquet purus posuere luctus.

---

This is a link to https://example.com.

[Assemble](http://assemble.io)

[Upstage](https://github.com/upstage/ "Visit Upstage!")

[Example][somelinkID]

[somelinkID]: https://example.com "Go to example domain"

---

Footnotes

That's some text with a footnote[^1]

[^1]: And that's the footnote.

That's some more text with a footnote.[^someid]

[^someid]:
    Anything of interest goes here.

Blue light glows blue.
