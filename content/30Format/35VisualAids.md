---
title: "Visual Aids"
weight: 35
---

Visual aids are a key component to conveying instruction clearly. Screenshots of UI allow users to quickly compare the directions to their lab environments, and allow users to orient themselves as they're exploring the topic being taught.

---

## Image Guidelines

For loadability and readability, the following guidelines should be followed:
  - [x] Images should be no more then 200kb in size.
  - [x] Images should be no more than 800px wide.
  - [x] Images should **always** contain alt text.

Following these guidelines help ensure that images are viewable across a wide variety of devices, and help ensure excessive bandwidth requirements during training aren't neccesary. 

---

#### JPG or PNG?

Depending on the settings of your computer, you may be capturing screenshots in JPG or PNG format. PNG offers the ability to zoom into the image with much more detail and clarity, which is useful for diagrams and other images containing dense amounts of information. When capturing UI elements, JPG will often convey the same information, while taking less resources to load and process. 

---

{{% notice style="note" title="Image Storage" %}}
There are a few options when storing images (find more in depth discussion in the default repo). In this repo, the images have been stored in a seperate `images` directory under the `/content` directory.

- **Option 1:** use externally fully qualified absolutely path (this can be a pain)
- **Option 2:** if you have a directory with all your images.... 
  - put it in "/content/images"
  - MD usage(from a chapter page in "content/chapter01") 
    ```
        ![Magic](../images/magic.gif)
    ```
- **Option 3:**  Some find it easier to organize images with the pages they go with (this is how the template repo is setup)
  - put images in the chapter directory
  - e.g. images in "/content/chapter1/"
    - Markdown usage:
        ```
            ![Magic](magic.gif)
        ```

{{% /notice %}}

---

#### About CLI Capture

Whenever possible, it is desirable to capture the CLI output in [fenced code blocks]({{< relref "15markdown.md#fenced-code-block" >}}). By avoiding screenshots of text information, we reduce load times and improve readability across all devices. The primary exception to this would be when graphical information is shown via CLI, which may not format correctly if put into a fenced code block. If capturing screenshots of your CLI output is required, one should ensure a standard CLI window size of 80 characters wide by 24 lines tall is used to capture this information. Please also ensure your images adhere to the above guidance of 800px wide, and an image size of under 200kb.

---

## Embedded Images

Images have a similar syntax to [links]({{< relref "15markdown.md#links" >}}) but include a preceding exclamation mark. Like [links]({{< relref "15markdown.md#links" >}}), images can also be given a tooltip. Keep reading for examples of how to add both.

#### Alt Text
Alt text is contained in the square `[]` brackets, and every effort should be made to include alternate text. [Good guidelines](https://www.w3.org/WAI/tutorials/images/decision-tree/) on when to include or omit alt text, and what content should be there is provided by W3C.

---

#### Classes and Image Effects

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
Adjust your browser height/width to see how these settings affect images differently:    
**20vw:**
![20 vw setting](../images/trekkie.jpg?width=20vw "20% viewing width")
**20vh:**
![20 vh setting](../images/trekkie.jpg?width=20vh "20% viewing height")
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

