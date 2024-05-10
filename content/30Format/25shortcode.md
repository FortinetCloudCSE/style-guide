---
title: "Shortcode"
weight: 25
---

## Badge

The `badge` shortcode displays little markers in your text with adjustable color, title and icon. Under prerequisites or introduction to labs we should include a badge highlighting software version for Fortinet software (if applicable). Check for readability against the theme you're using. Notice the example below of white text on yellow is difficult to read in light mode.

Full parameters for badges can be [found here](https://mcshelby.github.io/hugo-theme-relearn/shortcodes/badge/index.html#parameter).

### Example badges:

````go
{{%/* badge %}}Important{{% /badge */%}}
{{%/* badge style="primary" title="FortiGate Version" %}}7.2.8{{% /badge */%}}
{{%/* badge style="red" icon="angle-double-up" %}}AWS{{% /badge */%}}
{{%/* badge style="info" %}}New in 7.4{{% /badge */%}}
{{%/* badge color="fuchsia" icon="fa-fw fab fa-hackerrank" %}}Awesome{{% /badge */%}}
{{%/* badge style="primary" icon="bullhorn" title="Announcement" %}}Mandatory{{% /badge */%}}
{{%/* badge style="secondary" icon="bullhorn" title="Announcement" %}}Optional{{% /badge */%}}
{{%/* badge style="accent" icon="bullhorn" title="Announcement" %}}Special{{% /badge */%}}
````

{{% notice style="secondary" icon="eye" title="Result" %}}
{{% badge %}}Important{{% /badge %}}
{{% badge style="primary" title="FortiGate Version" %}}7.2.8{{% /badge %}}
{{% badge style="red" icon="angle-double-up" %}}AWS{{% /badge %}}
{{% badge style="info" %}}New in 7.4{{% /badge %}}
{{% badge color="fuchsia" icon="fa-fw fab fa-hackerrank" %}}Awesome{{% /badge %}}

{{% badge style="primary" icon="bullhorn" title="Announcement" %}}Mandatory{{% /badge %}}
{{% badge style="secondary" icon="bullhorn" title="Announcement" %}}Optional{{% /badge %}}
{{% badge style="accent" icon="bullhorn" title="Announcement" %}}Special{{% /badge %}}
{{% /notice %}}

---

## Button

The button shortcode displays a clickable button with adjustable color, title and icon. Use this for links you expect users to click on (they will open in a new page).

{{% button href="https://gohugo.io/" %}}Get Hugo{{% /button %}} {{% button href="https://gohugo.io/" style="warning" icon="dragon" %}}Get Hugo{{% /button %}}

```
{{%/* button href="https://gohugo.io/" %}}Get Hugo{{% /button */%}}
{{%/* button href="https://gohugo.io/" style="warning" icon="dragon" %}}Get Hugo{{% /button */%}}
```

You can read more about [buttons here](https://mcshelby.github.io/hugo-theme-relearn/shortcodes/button/index.html)

---

## Expand

The expand option lets you add additional detail, text, and images while keeping a page tidy and relatively short. Use of the expand option is encouraged for all step-by-step instruction during labs. In those labs, objectives should be stated, while step by step instruction to achieving those objectives should be held in an expand field, allowing users to attempt the lab on their own. This allows users to try themselves, but if they get stuck or lost on a specific part, they can expand the field and recieve step by step instruction.

```go
{{%/* expand title="**Detailed Steps...**" */%}}
- **1.1:** In your AWS account, navigate to the **EC2 Console** and go to the **Instances page** (menu on the left).
- **1.2:** Find the **ExPub-Instance1** instance, and copy the **Public IP address**.
- **1.3:** In your command prompt or terminal, ping the **public IPv4 address** of the instance.
   - This **SHOULD NOT** work at this point.
{{%/* /expand */%}}
```

{{% badge icon="eye" %}}Result:{{% /badge %}}
{{% expand title="**Detailed Steps...**" %}}

- **1.1:** In your AWS account, navigate to the **EC2 Console** and go to the **Instances page** (menu on the left).
- **1.2:** Find the **ExPub-Instance1** instance, and copy the **Public IP address**.
- **1.3:** In your command prompt or terminal, ping the **public IPv4 address** of the instance.
  - This **SHOULD NOT** work at this point.
{{% /expand %}}

**Author note:** _For some reason the notice box breaks when wrapped around an expand field - apologies for the inconsistency_

---

## Icon

The `icon` shortcode displays icons using the [Font Awesome](https://fontawesome.com/) library. This field is used extensively throughout the shortcode supported in this theme. 

Feel free to browse [Font Awesomes library](https://fontawesome.com/v5/search?m=free) and use what you need. Notice that the **free** filter is enabled, as only the free icons are available by default. Once on the Font Awesome page for a specific icon, for example the page for the [heart](https://fontawesome.com/v5/icons/heart?s=solid), copy the icon name and paste into the Markdown content.

### Example

````go
{{%/* icon exclamation-triangle */%}}
{{%/* icon angle-double-up */%}}
{{%/* icon skull-crossbones */%}}
````
{{% notice style="secondary" icon="eye" title="Result" %}}
{{% icon exclamation-triangle %}}{{% icon angle-double-up %}}{{% icon skull-crossbones %}}
{{% /notice %}}

---

## Mermaid

Mermaid is scripting language that lets you create simple diagrams and charts.

_Whenever possible_, a mermaid diagram is preferrable to a screenshot of one. However, its understood that Mermaid could be considered an advanced topic, and Mermaid diagrams are never required.

[Full documentation of Mermaid can be found here.](http://mermaid.js.org/intro/getting-started.html)

### Example

```go
{{</* mermaid align="center" zoom="true" */>}}
graph LR;
    If --> Then
    Then --> Else
{{</* /mermaid */>}}
```

{{% notice style="secondary" icon="eye" title="Result" %}}
{{< mermaid align="center" zoom="true" >}}
graph LR;
    If --> Then
    Then --> Else
{{< /mermaid >}}
{{% /notice %}}

---

## Notice

Notice boxes are great for highlighting specific results for a section of code. These are used extensively throughout this doc to show what example code renders to look like. These are great ways to show off what should happen, or explain why something occured the way it did in your lab. To create a notice box see the example below

```go
{{%/* notice style="secondary" icon="eye" title="Result" */%}}
This is the notice box
{{%/* /notice */%}}
```
{{% notice style="secondary" icon="eye" title="Result" %}}
This is the notice box
{{% /notice %}}

---

### Other Default Boxes:

There's a handful of notice boxes pre-defined within the theme and available for use with minimal code. However there are [extensive customizations available](https://mcshelby.github.io/hugo-theme-relearn/shortcodes/notice/index.html).

```go
{{%/* notice note */%}}
This is the note box
{{%/* /notice */%}}
```
{{% notice note %}}
This is the note box
{{% /notice %}}

---

```go
{{%/* notice style="info" */%}}
This is the info box
{{%/* /notice */%}}
```
{{% notice style="info" %}}
This is the info box
{{% /notice %}}

---

```go
{{%/* notice style="warning" */%}}
This is the warning box
{{%/* /notice */%}}
```
{{% notice style="warning" %}}
This is the warning box
{{% /notice %}}

---

```go
{{%/* notice style="tip" */%}}
This is the tip box
{{%/* /notice */%}}
```
{{% notice style="tip" %}}
This is the tip box
{{% /notice %}}
