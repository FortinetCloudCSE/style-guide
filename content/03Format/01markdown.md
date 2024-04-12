---
title: "Markdown"
chapter: True
menuTitle: "Markdown"
weight: 15
---

# Markdown

## Purpose

This section is built to provide guidance on how to use markdown, and when to use specific markdown types.

---

## Headers

Headers are the primary way of establishing order on the pages, and is used to designate the purpose of a section. Each section should start with a header, and end with a line break.

To create a header, on a new line simply place the appropriate number of `#` followed by a space, followed by the words of the header. There are 6 types of headers, designate H1 through H6. Headers 1 (H1) through 4 (H4) are used like indents in an outline. There should be 1 H1 per page, and an H2 per section. If each section is divided into subsections, H3 or H4 can be used.

Below you will find examples of the various headers, and in the grey textbox, you will find the sample markdown to create the header demonstrated.

#### Example Headers:

# Chapter 1 (Header 1)

In markdown, this header looks like this:

    # Chapter 1 (Header 1)


H1 headers aren't generally used, because Hugo renders the titles automatically. H1 headers should only be used for the title of the page. If you find the need to use a second H1 header, consider breaking that off into a seperate page. Notice how this puts it in all capitals, centers the text, and adds a line break underneath it.

**Note:** H1 headers should only be used in chapters, as the `Title` field is rendered as the H1 header when editing the _index.md for a top level heading.

---

## Chapter 1 Section 1 (Header 2)

In markdown, you can generate this type of header like this:

    ## Chapter 1 Section 1 (Header 2)


H2 headers should be used to signal the beginning of a section. A section should be useful on its own, and can be linked directly from other sources. Notice that we lose all capitalization, the size is smaller, and there is no line break underneath it. Each chapter should contain a few sections at minimum.

---

### Action Items (Header 3)
In markdown, you can generate this type of header like this:

    ### Action Items (Header 3)

H3 is meant to use to divide instruction from doing. This could be a summary of the section, a set of review questions to explore and test knowledge, or lab instructions for extra credit or exploring on their own. This should be used within the section to designate 'hands on' activities.

---

#### Chapter 1 Section 1 Subsection A (Header 4)

In markdown, you can generate this type of header like this:

    #### Chapter 1 Section 1 Subsection (Header 4)

Lastly, H4 headers are for use as a subsection title. These can be used to break up topics that all pertain to a given section.

---

There are 2 other supported headers, H5 and H6.

##### H5 Headers:
H5 headers currently don't have a designated use, but is provided to help break up and logically organize dense sections of information as needed. They are coded with 5 `#` in a row, like this:

    ##### H5 Headers:

---

###### H6 headers:

H6 should be used to title images and tables. This is useful because it provides a link directly to the image or table later as needed. They are coded with 6 `#` in a row, like this:

    ###### H6 Headers:

---

## Text Stylization

All basic formatting is available via markdown. This section will walk you through how to create that formatting, as well as when to use specific types, so that we can consistently message expectations to the end user.

When typing things, theres **bold text**, _italicized text_, ~~strike through~~. To show this, you wrap the words with `**`, `_`, or `~~` respectively. The first sentence in this paragraph looks like this in markdown:

    When typing things, theres **bold text**, _italicized text_, ~~strike through~~.

## Horizontal Rules

To further structure your content you can add horizontal rules. They create a "thematic break" between paragraph blocks. In Markdown, you can create it with three consecutive dashes `---`.

````md
Lorem ipsum dolor sit amet, graecis denique ei vel, at duo primis mandamus.

---

Et legere ocurreret pri, animal tacimates complectitur ad cum. Cu eum inermis inimicus efficiendi. Labore officiis his ex, soluta officiis concludaturque ei qui, vide sensibus vim ad.
````

{{% notice style="secondary" icon="eye" title="Result" %}}
Lorem ipsum dolor sit amet, graecis denique ei vel, at duo primis mandamus.

---

Et legere ocurreret pri, animal tacimates complectitur ad cum. Cu eum inermis inimicus efficiendi. Labore officiis his ex, soluta officiis concludaturque ei qui, vide sensibus vim ad.
{{% /notice %}}

## Keyboard Shortcuts

You can use the `<kbd>` element to style keyboard shortcuts.

````html
Press <kbd>CTRL</kbd> <kbd>ALT</kbd> <kbd>DEL</kbd> to end your shift early.
````

{{% notice style="secondary" icon="eye" title="Result" %}}
Press <kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>DEL</kbd> to end your shift early.
{{% /notice %}}


## Code and CLI

There will often be times when direction to the reader is neccessary for action within a UI or CLI. When directing a user to navigate a UI, you should **bold** the words or buttons to click on. When directing action via CLI, we have several capabilities for including code in our documentation, listed below.

#### Inline Code

Inline snippets of code can be wrapped with backticks `` ` ``.

````md
In this example, `<div></div>` is marked as code.
````

{{% notice style="secondary" icon="eye" title="Result" %}}
In this example, `<div></div>` is marked as code.
{{% /notice %}}

#### Indented Code Block

A simple code block can be generated by indenting several lines of code by at least two spaces.

````md
Be impressed by my advanced code:

    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code
````

{{% notice style="secondary" icon="eye" title="Result" %}}
Be impressed by my advanced code:

    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code
{{% /notice %}}

#### Fenced Code Block

If you want to gain more control of your code block you can enclose your code by at least three backticks ```` ``` ```` a so called fence.

You can also add a language specifier directly after the opening fence, ` ```js `, and syntax highlighting will automatically be applied according to the selected language in the rendered HTML. This can be especially useful in combination with tabs, which is discussed in the shortcode section.

````plaintext
```js
{
    name: "Claus",
    surname: "Santa",
    profession: "courier",
    age: 666,
    address: {
        city: "North Pole",
        postalCode: 1,
        country: "Arctic"
    },
    friends: [ "Dasher", "Dancer", "Prancer", "Vixen", "Comet", "Cupid", "Donder", "Blitzen", "Rudolph" ]
};
```
````

{{% notice style="secondary" icon="eye" title="Result" %}}
```js
{
    name: "Claus",
    surname: "Santa",
    profession: "courier",
    age: 666,
    address: {
        city: "North Pole",
        postalCode: 1,
        country: "Arctic"
    },
    friends: [ "Dasher", "Dancer", "Prancer", "Vixen", "Comet", "Cupid", "Donder", "Blitzen", "Rudolph" ]
};
```
{{% /notice %}}

{{% notice style="secondary" icon="eye" title="Note" %}}
 When not using code blocks, double quotes `"` and single quotes `'` of enclosed text are replaced by **"double curly quotes"** and **'single curly quotes'**. Double dashes `--` and triple dashes `---` are replaced by en-dash **--** and em-dash **---** entities. Double arrows pointing left `<<` or right `>>` are replaced by arrow **<<** and **>>** entities. Three consecutive dots `...` are replaced by an ellipsis **...** entity. **This can impact things when expecting users to copy and paste text into their lab environments.**
{{% /notice %}}

---

## Lists
You can write a list of items in which the order of the items does not explicitly matter.

It is possible to nest lists by indenting an item for the next sublevel.

You may use any of `-`, `*` or `+` to denote bullets for each list item but should not switch between those symbols inside one whole list.

#### Unordered List
```
- Lorem ipsum dolor sit amet
- Consectetur adipiscing elit
  - Vestibulum laoreet porttitor sem
  - Ac tristique libero volutpat at
- Nulla volutpat aliquam velit
  - Phasellus iaculis neque
  - Purus sodales ultricies
- Faucibus porta lacus fringilla vel
```

{{% notice style="secondary" icon="eye" title="Result" %}}
- Lorem ipsum dolor sit amet
- Consectetur adipiscing elit
  - Vestibulum laoreet porttitor sem
  - Ac tristique libero volutpat at
- Nulla volutpat aliquam velit
  - Phasellus iaculis neque
  - Purus sodales ultricies
- Faucibus porta lacus fringilla vel
{{% /notice %}}

---
#### Ordered lists

You can create a list of items in which the order of items does explicitly matter.

It is possible to nest lists by indenting an item for the next sublevel.

Markdown will automatically number each of your items consecutively. This means, the order number you are providing is irrelevant.
```
1. Lorem ipsum dolor sit amet
3. Consectetur adipiscing elit
    1. Integer molestie lorem at massa
    7. Facilisis in pretium nisl aliquet
99. Nulla volutpat aliquam velit
    1. Faucibus porta lacus fringilla vel
    1. Aenean sit amet erat nunc
17. Eget porttitor lorem
```

{{% notice style="secondary" icon="eye" title="Result" %}}
1. Lorem ipsum dolor sit amet
3. Consectetur adipiscing elit
    1. Integer molestie lorem at massa
    7. Facilisis in pretium nisl aliquet
99. Nulla volutpat aliquam velit
    1. Faucibus porta lacus fringilla vel
    1. Aenean sit amet erat nunc
17. Eget porttitor lorem
{{% /notice %}}

---

#### Task lists

You can add task lists resulting in checked or unchecked non-clickable items

```
- [x] Basic Test
- [ ] More Tests
  - [x] View
  - [x] Hear
  - [ ] Smell
```

{{% notice style="secondary" icon="eye" title="Result" %}}
- [x] Basic Test
- [ ] More Tests
  - [x] View
  - [x] Hear
  - [ ] Smell
{{% /notice %}}

---

## Definitions

Definition lists are made of terms and definitions of these terms, much like in a dictionary.

A definition list in Markdown Extra is made of a single-line term followed by a colon and the definition for that term. You can also associate more than one term to a definition.

If you add empty lines around the definition terms, additional vertical space will be generated. Also multiple paragraphs are possible

```
Apple
: Pomaceous fruit of plants of the genus Malus in the family Rosaceae.
: An American computer company.

Orange
: The fruit of an evergreen tree of the genus Citrus.

  You can make juice out of it.
: A telecommunication company.

  You can't make juice out of it.
```

{{% notice style="secondary" icon="eye" title="Result" %}}
Apple
: Pomaceous fruit of plants of the genus Malus in the family Rosaceae.
: An American computer company.

Orange
: The fruit of an evergreen tree of the genus Citrus.

  You can make juice out of it.
: A telecommunication company.

  You can't make juice out of it.
{{% /notice %}}

---

## Tables

You can create tables by adding pipes as dividers between each cell, and by adding a line of dashes (also separated by bars) beneath the header. Note that the pipes do not need to be vertically aligned. Adding a colon on the left and/or right side of the dashes below any heading will align the text for that column accordingly.

```
| Option | Number | Description |
|-------:|:------:|:------------|
| data   | 1      | path to data files to supply the data that will be passed into templates. |
| engine | 2      | engine to be used for processing templates. Handlebars is the default. |
| ext    | 3      | extension to be used for dest files. |
```

{{% notice style="secondary" icon="eye" title="Result" %}}
| Option | Number | Description |
|-------:|:------:|:------------|
| data   | 1      | path to data files to supply the data that will be passed into templates. |
| engine | 2      | engine to be used for processing templates. Handlebars is the default. |
| ext    | 3      | extension to be used for dest files. |
{{% /notice %}}

---

## Block Quotes
For quoting blocks of content from another source within your document add `>` before any text you want to quote.

Blockquotes can also be nested.

```
> Donec massa lacus, ultricies a ullamcorper in, fermentum sed augue. Nunc augue, aliquam non hendrerit ac, commodo vel nisi.
>
> > Sed adipiscing elit vitae augue consectetur a gravida nunc vehicula. Donec auctor odio non est accumsan facilisis. Aliquam id turpis in dolor tincidunt mollis ac eu diam.
>
> Mauris sit amet ligula egestas, feugiat metus tincidunt, luctus libero. Donec congue finibus tempor. Vestibulum aliquet sollicitudin erat, ut aliquet purus posuere luctus.
```

{{% notice style="secondary" icon="eye" title="Result" %}}
> Donec massa lacus, ultricies a ullamcorper in, fermentum sed augue. Nunc augue, aliquam non hendrerit ac, commodo vel nisi.
>
> > Sed adipiscing elit vitae augue consectetur a gravida nunc vehicula. Donec auctor odio non est accumsan facilisis. Aliquam id turpis in dolor tincidunt mollis ac eu diam.
>
> Mauris sit amet ligula egestas, feugiat metus tincidunt, luctus libero. Donec congue finibus tempor. Vestibulum aliquet sollicitudin erat, ut aliquet purus posuere luctus.
{{% /notice %}}

---
## Links

#### Autolink

Absolute URLs will automatically be converted into a link.

````md
This is a link to https://example.com.
````

{{% notice style="secondary" icon="eye" title="Result" %}}
This is a link to https://example.com.
{{% /notice %}}


#### Basic Link

You can explicitly define links in case you want to use non-absolute URLs or want to give different text.

````md
[Assemble](http://assemble.io)
````

{{% notice style="secondary" icon="eye" title="Result" %}}
[Assemble](http://assemble.io)
{{% /notice %}}

#### Link with Tooltip

For even further information, you can add an additional text, displayed in a tooltip on hovering over the link.

````md
[Upstage](https://github.com/upstage/ "Visit Upstage!")
````

{{% notice style="secondary" icon="eye" title="Result" %}}
[Upstage](https://github.com/upstage/ "Visit Upstage!")
{{% /notice %}}

#### Link References

Links can be simplyfied for recurring reuse by using a reference ID to later define the URL location. This simplyfies writing if you want to use a link more than once in a document.

````md
[Example][somelinkID]

[somelinkID]: https://example.com "Go to example domain"
````

{{% notice style="secondary" icon="eye" title="Result" %}}
[Example][somelinkID]

[somelinkID]: https://example.com "Go to example domain"
{{% /notice %}}

#### Footnotes

Footnotes work mostly like reference-style links. A footnote is made of two things, a marker in the text that will become a superscript number and a footnote definition that will be placed in a list of footnotes.

Usually the list of footnotes will be shown at the end of your document. If we use a footnote in a notice box it will instead be listed at the end of its box.

Footnotes can contain block elements, which means that you can put multiple paragraphs, lists, blockquotes and so on in a footnote. It works the same as for list items, just indent the following paragraphs by four spaces in the footnote definition.

````md
That's some text with a footnote[^1]

[^1]: And that's the footnote.

That's some more text with a footnote.[^someid]

[^someid]:
    Anything of interest goes here.

    Blue light glows blue.
````

{{% notice style="secondary" icon="eye" title="Result" %}}
That's some text with a footnote[^1]

[^1]: And that's the footnote.

That's some more text with a footnote.[^someid]

[^someid]:
    Anything of interest goes here.

    Blue light glows blue.
{{% /notice %}}

