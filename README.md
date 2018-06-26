# NativeScript Playground Tutorials

This repo contains the tutorials that appear in [NativeScript Playground](https://play.nativescript.org/).

## Tutorial structure

All tutorials live in the root of the repo and conform to the following structure.

```
name-of-tutorial
├── 1.md
├── 2.md
├── 3.md
├── ...
├── images
│   ├── image-1.png
│   └── ...
├── metadata.json
└── success.md
```

Each tutorial’s content should be divided into lessons and steps, and each lesson should be placed into a sequentially named Markdown file. For example, a tutorial’s first lesson should live in a file named `1.md`, a tutorial’s second lesson should live in a file named `2.md`, and so on.

The content of each lesson should follow the following pattern.

```
## Lesson 1. Name of First Lesson

[an introduction to the lesson]

### Step 1. Name of first step

[the contents of the step]

### Step 2. Name of second step

[the contents of the step]
```

All steps you wish a user to complete should appear within a step, and should use the following structure.

```
[text to introduce what the user needs to do in the action section]

<hr data-action="start" />

#### Action

* **a.** The first step the user needs to do.

* **b.** The second step the user needs to do.

* **c.** ...

<hr data-action="end" />
```

> **NOTE**: Playground gives the user the ability to copy and paste any code blocks you provide in Action sections.

The last thing to note about a tutorial’s content is its `success.md` file. Playground shows the content you place in this file after the user completes the tutorial. You probably want to either link to another tutorial here, or to recommend additional resources or next steps for the reader.

## Tutorial metadata

In addition to content, each tutorial should have a `metadata.json` file with the following content.

```
{
  "title": "The Tutorial’s Title",
  "description": "A short description of the tutorial",
  "estimateTime": "15",
  "displayOrder": 1,
  "supportedTemplates": ["play-ng"],
  "targetTemplate": "play-ng",
  "disabled": false
}
```

Here is some more information on some of the additional keys.

* `estimateTime`—The approximate amount of time you believe it will take a user to complete the tutorial in minutes.
* `displayOrder`—The order the tutorial should appear in relation to other tutorials. Note that the JS, Angular, and Vue.js tutorials are all in separate buckets, so you want to compare the tutorial you’re working on with others for the same framework.
* `supportedTemplates`—An array of templates the tutorial supports. Normally this is identical to the tutorial’s `targetTemplate`.
* `targetTemplate`—The name of the template your tutorial uses as its starting point. Currently these templates are private, so work with the NativeScript team in a pull request to get the appropriate template in place.
* `disabled`—Whether the tutorial should be disabled.

