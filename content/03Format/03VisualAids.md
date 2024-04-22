---
title: "Visual Aids"
chapter: True
menuTitle: "Visual Aids"
weight: 35
---

# Visual Aids

Visual aids are a key component to conveying instruction clearly. Screenshots of UI allow users to quickly compare the directions to their lab environments, and allow users to orient themselves as they're exploring the topic being taught.

## Image Guidelines

For loadability and readability, the following guidelines should be followed:
  - Images should be no more then 200kb in size.
  - Images should be no more than 800px wide.

Following these guidelines help ensure that images are viewable across a wide variety of devices, and help ensure excessive bandwidth requirements during training aren't neccesary. 

{{% notice tip %}}

###### JPG or PNG?
Depending on the settings of your computer, you may be capturing screenshots in JPG or PNG format. PNG offers the ability to zoom into the image with much more detail and clarity, which is useful for diagrams and other images containing dense amounts of information. When capturing UI elements, JPG will often convey the same information, while taking less resources to load and process. 

{{% /notice %}}

---

## Embedded Images

Images have a similar syntax to [links]({{< relref "01markdown.md#links" >}}) but include a preceding exclamation mark. Like [links]({{< relref "01markdown.md#links" >}}), images can also be given a tooltip.

---

## Alt Text
Alt text is contained in the square `[]` brackets, and every effort should be made to include alternate text. [Good guidelines](https://www.w3.org/WAI/tutorials/images/decision-tree/) on when to include or omit alt text, and what content should be there is provided by W3C.

---

## Classes and Image Effects

Several classes are available, which can be appended to images to manipulate them to ensure they display as you expect them to. You can append classes to images by adding `?` followed by the class name, then your definition. You can append multiple classes by adding `&` between them. These include:

| Class name | What it does |
|---|---|
| `width` | defines the width of the image when displayed. Can be defined in absolute size by defining `px` (pixels) or relative size with `vw` (% of viewing width) |
| `height` | defines the height of the image when displayed. Similar to width, can be defined by `px` or in relative height with **`vh`**  |
| `classes` | Defines alignment of the image. Can use `left` and `right` for page alignemnt, and `inline` for adding multiple images to a single line |

###### Image Examples
````md
Alt Text and Tooltip implemented
![This is alt text](../images/spocktocat.png "This is a tooltip")
Adjust your browser height/width to see how these settings affect images:
![This is alt text](../images/trekkie.jpg?width=20vw "20% viewing width")
![This is alt text](../images/trekkie.jpg?width=20vh "20% viewing height")
````

{{% notice style="secondary" icon="eye" title="Result" %}}
Alt Text and Tooltip implemented
![This is alt text](../images/spocktocat.png "This is a tooltip")
Adjust your browser height/width to see how these settings affect images:
![This is alt text](../images/trekkie.jpg?width=20vw "20% viewing width")
![This is alt text](../images/trekkie.jpg?width=20vh "20% viewing height")
{{% /notice %}}

###### Class Definitions:
````md
Left Alignment:   

![Left Aligned](../images/droctocat.png?classes=left&width=10vw  "Left Aligned")

Right Alignment:    

![Right Aligned](../images/droctocat.png?classes=right&width=10vw  "Right Aligned")

Inline Alignment:    

![Inline example 1](../images/droctocat.png?classes=inline&width=10vw  "Inline example 1") ![Inline example 2](../images/trekkie.jpg?classes=inline&width=10vw  "Inline example 2")
````

{{% notice style="secondary" icon="eye" title="Result" %}}
Left Alignment:

![Left Aligned](../images/droctocat.png?classes=left&width=10vw "Left Aligned")

Right Alignment:

![Right Aligned](../images/droctocat.png?classes=right&width=10vw "Right Aligned")

Inline Alignment:  

![Inline example 1](../images/droctocat.png?classes=inline&width=10vw  "Inline example 1") ![Inline example 2](../images/trekkie.jpg?classes=inline&width=10vw  "Inline example 2")
{{% /notice %}}