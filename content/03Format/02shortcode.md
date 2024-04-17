---
title: "Shortcode"
chapter: True
menuTitle: "Shortcode"
weight: 25
---

# Shortcode

## Badge

The `badge` shortcode displays little markers in your text with adjustable color, title and icon. Under prerequisites or introduction to labs we should include a badge highlighting software version for Fortinet software (if applicable). Check for readability against the theme you're using. Notice the example below of white text on yellow is difficult to read in light mode.

Full parameters for badges can be [found here](https://mcshelby.github.io/hugo-theme-relearn/shortcodes/badge/index.html#parameter).

###### Example badges:

````go
{{%/* badge %}}Important{{% /badge */%}}
{{%/* badge style="primary" title="Version" %}}6.6.6{{% /badge */%}}
{{%/* badge style="red" icon="angle-double-up" %}}Captain{{% /badge */%}}
{{%/* badge style="info" %}}New{{% /badge */%}}
{{%/* badge color="fuchsia" icon="fa-fw fab fa-hackerrank" %}}Awesome{{% /badge */%}}
{{%/* badge style="primary" icon="bullhorn" title="Announcement" %}}Mandatory{{% /badge */%}}
{{%/* badge style="secondary" icon="bullhorn" title="Announcement" %}}Optional{{% /badge */%}}
{{%/* badge style="accent" icon="bullhorn" title="Announcement" %}}Special{{% /badge */%}}
````

{{% notice style="secondary" icon="eye" title="Result" %}}
{{% badge %}}Important{{% /badge %}}
{{% badge style="primary" title="Version" %}}6.6.6{{% /badge %}}
{{% badge style="red" icon="angle-double-up" %}}Captain{{% /badge %}}
{{% badge style="info" %}}New{{% /badge %}}
{{% badge color="fuchsia" icon="fa-fw fab fa-hackerrank" %}}Awesome{{% /badge %}}

{{% badge style="primary" icon="bullhorn" title="Announcement" %}}Mandatory{{% /badge %}}
{{% badge style="secondary" icon="bullhorn" title="Announcement" %}}Optional{{% /badge %}}
{{% badge style="accent" icon="bullhorn" title="Announcement" %}}Special{{% /badge %}}
{{% /notice %}}

## Button
## Expand
## Icon

The `icon` shortcode displays icons using the [Font Awesome](https://fontawesome.com/) library. This field is used extensively throughout the shortcode supported in this theme. 

Feel free to browse [Font Awesomes library](https://fontawesome.com/v5/search?m=free) and use what you need. Notice that the **free** filter is enabled, as only the free icons are available by default. Once on the Font Awesome page for a specific icon, for example the page for the [heart](https://fontawesome.com/v5/icons/heart?s=solid), copy the icon name and paste into the Markdown content.

###### Example
````go
{{%/* icon exclamation-triangle */%}}
{{%/* icon angle-double-up */%}}
{{%/* icon skull-crossbones */%}}
````
{{% notice style="secondary" icon="eye" title="Result" %}}
{{% icon exclamation-triangle %}}{{% icon angle-double-up %}}{{% icon skull-crossbones %}}
{{% /notice %}}

## Mermaid
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

## Tabs
