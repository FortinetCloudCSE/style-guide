---
title: "Format and Structure"
chapter: true
menuTitle: "III: Format and Structure"
weight: 30
---

## Purpose

This section covers the code and content for formatting your pages, organizing your data, and using markdown to convey your options to users clearly.

## too long; didn't read
###### Markdown
- [Headers]({{< relref "15markdown.md#headers" >}})
  - H1 headers are not needed on index pages, but may be added to any pages containing the configuration `chapter: false`
  - H2 headers begin a new section in a page
  - H3 headers highlight action items for the user
  - H4 headers are for subsections within sections
  - H5 headers may be used at your discretion as needed
  - H6 headers are used to title tables and images
- Use [Horizontal Rules]({{< relref "15markdown.md#horizontal-rules" >}}) to break up sections
- Use **Bold** text when a user should click that option in the UI
- Use [inline code]({{< relref "15markdown.md#code-and-cli" >}}) when referencing a CLI command or syntax
  - **Not when instructing users to type it!**
- Use [code blocks]({{< relref "15markdown.md#indented-code-block" >}}) when providing commands for user input, as well as when capturing CLI output.
- [Unordered lists]({{< relref "15markdown.md#unordered-lists" >}}) are great for providing quick, easily digested summaries (like this)
- [Ordered]({{< relref "15markdown.md#ordered-lists" >}}) and [task lists]({{< relref "15markdown.md#task-lists" >}}) should be used for objectives and review of labs
- [Definitions]({{< relref "15markdown.md#definitions" >}}) are useful when introducing new vocabulary or concepts.
- [Tables]({{< relref "15markdown.md#tables" >}}) are usefull for comparing and contrasting different technologies
- [Block quotes]({{< relref "15markdown.md#block-quotes" >}}) can be used for quoting other sections or even other source material
  - Use [footnotes]({{< relref "15markdown.md#footnotes" >}}) to link the source!
- Everything to know about [links]({{< relref "15markdown.md#links" >}}) can be found here.

###### ShortCodes
  - [Badges]({{< relref "25shortcode.md#badge" >}}) should be used to denote firmware or cloud specific information, but can be used creatively to convey any other variations in instruction as needed.
  - [Buttons]({{< relref "25shortcode.md#badge" >}}) provide a way to guide users to additional resources in another tab. Useful for opening external resources, such as Qwik Labs or CSP Consoles.
  - [Expand]({{< relref "25shortcode.md#expand" >}}) is a convenient way to add verbose information without clutering a page.
  - [Icons]({{< relref "25shortcode.md#icon" >}}) are used throughout shortcode, providing simple graphics to help denote specific information.
  - [Mermaid]({{< relref "25shortcode.md#mermaid" >}}) allows for diagrams and charts to be drawn dynamically, rather then relying on images.
  - [Notice]({{< relref "25shortcode.md#notice" >}}) boxes provide information specific to the lab. Such as the **Result** boxes shown throughout this document.
  
