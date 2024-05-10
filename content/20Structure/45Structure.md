---
title: "Content Structure"
weight: 45
---

With the Fortinet-hugo theme, our content is broken down into chapters, with each chapter broken into sections. These sections are further broken down into subsections within each page.

When developing content, using the directory below can help ensure readability and consistency across all courses we create.

###### File Structure

```text
content
├── 01chapter-one
│   ├── _index.md                   <-- /01chapter-one.html
│   ├── 01section-a.md                 <-- /01chapter-one/01section-a.html
│   ├── 02section-b.md                 <-- /01chapter-one/02section-b.html
│   └── 03section-c.md                 <-- /01chapter-one/03section-c.html
├── 02chapter-two
│   ├── _index.md                   <-- /01chapter-one.html
│   ├── 01section-a.md                 <-- /02chapter-two/01section-a.html
│   ├── 02section-b.md                 <-- /02chapter-two/02section-b.html
│   └── 03section-c.md                 <-- /02chapter-two/03section-c.html
├── _index.md                       <-- /
└── 03chapter-three.md              <-- /03chapter-three.html
```

---

## Content Structure

Content should be broken into chapters, and contain the following at _minimum_, in this order.

1. Preface
2. Content ([Chapters]({{< relref "#chapters" >}}), split into [sections]({{< relref "#sections">}}))
3. (optional) Glossary
4. (optional) Appendices

### Preface

Every guide created should begin with a preface. The preface should provide a brief overview of the content of the guide. The preface should also contain any prerequisite knowledge the user should already have, and the learning objectives.

Learning objectives, sometimes called learning outcomes, are statements which clearly describe what is to be achieved by completion of the course. Clearly defined learning objectives also have the advantage of providing clarity to the authors, by providing the desired end state in the beginning.

Beyond the summary and learning objectives, the preface should also contain any lab logistics (e.g. _register and account on qwiklabs_), and if this event is being hosted in person, gives a place to provide any in-person logistics that may be useful or helpful.

### Content

The chapters of content are where the author will create most of their work.

On the `_index.md` page of a chapter, you should include an abstract and introduction to the chapter. Optionally you may also include links to frequently referenced areas within the sections.

The sections will contain the content of the guide, and there are primarily two ways to present this information; individual learning, and classroom learning. We explore both ways of organizing your content [in the style section]({{< relref "#style" >}}). Remember the [rule of three](https://en.wikipedia.org/wiki/Rule_of_three_(writing)) in learning, and try to adhere to this for maximal effectiveness.

Lastly, within each chapter, we want to include a review and troubleshooting section. This section should contain some questions that test the knowledge of the section, and include answers embedded in [expand shortcode]({{< relref "30format/25shortcode.md#expand" >}}) to keep the answers hidden until they're ready to read them. These questions should test general knowledge of what was covered, as well as frequently asked questions after the guide has had some use.

### Glossary

The glossary is, in fact, a type of appendix and is a list of terms found throughout the content. With the diversity of technologies covered by these guides, and the variety of experience each user may have, the glossary allows for a quick reference to common terms and phrases, and provides a location to add additional references for documentation that may help provide additional context.

The glossary included in this repo is written to be reused by other content. If there are other definitions or inclusions that should be added, please submit them.

### Appendices

Any other additional information that doesn't fit elsewhere in the document can be appended here. This could be more elaborate labs, white papers, and more.

### Contributors

As the last appendix of the guide, include a contributors chapter. This chapter should contain a change log. This change log allows for quick reference to major changes and rewrites that occur, and should allow easy pinpointing of changes or losses within the git version control system. This section should also contain a notice of process to submit your own changes to the documentation as needed. If needed, this is also where license information for the written content can be included as well.

---

## Style

There are two primary styles of content you'll strive to develop. Those two styles are **individual** and **classroom**. Its important to choose a style when begining your development, and to remain consistent. However, these styles may be interspersed as needed. For example, an extra credit portion may cover more advanced topics not discussed in a class, which would justify pivoting to an individual style for that chapter.

Individual
: This style is useful for _computer based training (CBT)_, or unguided types hands-on activities. Lab instructions are interspersed with instructional information. This style is frequently used for _immersion days_ and _jam_ type content. It may be preceded by a quick overview of what will be covered, but is primarily individual effort, with moderators to assist individuals when they have issues.

Classroom
: This style is to be used when presenting to a group, before then releasing them into their lab to recreate or gain hands on experience with what is discussed. When writing instructional content, the lab work should be concisely written after the content that is reviewed together.

### Examples

#### Individual Example Chapter

- Kubernetes Overview
  - Cluster Architecture
  - Containers
  - Nodes and Services

{{% notice note %}}
In this example, the lesson may include the basic components of Kubernetes, followed by deploying a managed kubernetes cluster (K8s Basics). Then in the Node and Service section, Node and Service concepts would be discussed, proceeded by walking the user through looking at those concepts in their deployed environment. The lab and instructional content are interspersed.
{{% /notice %}}

#### Classroom Example Chapter

- Kubernetes Overview
  - Cluster Architecture
  - Containers
  - Nodes and Services
  - Task 1 - Launch AKS
  - Task 2 - Navigating K8s by CLI

{{% notice note %}}
In this example, the lesson is divided into 3 sections of instructional content, followed by 2 tasks to accomplish in the lab. This lends itself well to classroom environments, as presenters can review the content interactively with everyone, prior to then having the group work independently through the hands-on portion.
{{% /notice %}}

## Chapters

A **chapter** displays a page meant to be used as introduction for a set of child pages. Commonly, it contains a simple title and a catch line to define content that can be found under it. Every course should contain a _minimum_ of 3 chapters.

We create content in markdown, and place these files into the `content` directory. To keep these organized, we create a new directory for each chapter, and an `_index.md` file is created inside it. This `_index.html` servers as the chapter introduction. Every `_index.md` file should begin with the following information included at the top of the page.

###### Example Inclusions

```text
---
title: "Structure, Grammar, Voice, and Tone "
chapter: True
menuTitle: "II: Structure, Voice, Tone"
weight: 20
---
```

- **title:** - is where the title of chapter is defined. This will appear on the top navigation bar, which shows users where they are in the site navigation tree. This is an important option for users on screens of narrow width (such as a tablet or phone).
- **chapter:** - This is a boolean value. When `chapter: true`, the page is reduced to a narrower width, and is designed to be a 'title page' for each chapter.
- **menuTitle:** - This is an optional field, which allows the left side navigation bar to contain a different wording than the title. We try to include numbers or numerals to help with navigation, since navigation can be confusing without them, as the order is defined by `weight`
- **weight:** - Weight is used to define the order of chapters and subchapters. Lower numbers have higher priority than higher ones. Generally we use increments of 10 during initial drafting, to ensure flexibility to include additional pages later as needed. In the example above, the weight is set to 20, for the second chapter.

For organizational reasons when building chapters and subchapters, we typically will label the files and directories with numeric values collaborating eqvilant to the weight of each chapter. These are for human readability of the pre-published code only. Order within the published app is set by the **weight** value of each file.

{{% notice note %}}
If a particular chapter is light on content, the directory structure can be omitted, and the markdown file can be placed directly in the content folder. It will require the value of `chapter:` to be set false, as `chapter: true` sets the theme to an introductory layout.

See the [file layout]({{< relref "#file-layout" >}}) section, where `chapter-three.md` represents this.
{{% /notice %}}

---

## Sections

Sections are where the bulk of content is created. You've broken the content down into chapters, and used the `_index.md` page to prepare the summary of the chapter. Now you will build out the content in sections. Each section should contain an entire concept or lesson.

Like chapters, you should strive for a _minimum_ of 3 sections per chapter of content. Prerequisites and appendices may not be applicable, but if you dont have at least 3 sections, consider condensing the content entirely to the chapter page, or further breaking down content into 3 sections.

Similar to `_index.md` pages, each subchapter should contain this information at the beginning of each file

```text
---
title: "Content Structure"
weight: 45
---
```

{{% notice note %}}
See the [example inclusions]({{< relref "#example-inclusions" >}}) earlier in the chapter to understand each field. For subchapters, `menuTitle` and `chapter: false` are optional fields. We also shifted the numbering schema by 5 digits, to allow quick differentiation between chapters and subchapters.
{{% /notice %}}
