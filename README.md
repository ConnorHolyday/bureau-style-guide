# Web boilerplate and style guide

This is the boilerplate for our web based projects.

## **Installation**

### Required assets in order to run the boilerplate

- [Install node](http://nodejs.org/download/)
- [Install gulp](https://github.com/gulpjs/gulp/blob/master/docs/getting-started.md)
- [Install sass](http://sass-lang.com/install)
- [Install sass globbing](https://github.com/chriseppstein/sass-globbing)

### Setup process

1. Clone the repository and fire up a terminal window inside the root folder

2. Type the following command:

```
$ npm install
```
3. The npm command should install without error. Next, run:

```
$ npm run
```
You will then be presented with the development scripts you have available to run.

* **Build** - This is a one-time run script which generates all of the assets. This script is mainly run in the post-deploy process.
* **Watch** - This enables the watch task on all assets, and triggers LiveReload.
* **Modernizr** - This is a dedicated script which runs Modernizr. Remember to manually add your test conditiions to the `gulpfile`
* **Styleguide** - This will generate a fresh styleguide under `/styleguide/`.

---

To run one of the above tasks, re-run the `$ npm run` command and add the task name, for example:

```
$ npm run watch
```

## **Optional Extras**

### Live Reload

In order to use livereload, you need to install the browser-extension. We use [Chrome](https://chrome.google.com/webstore/detail/livereload/jnihajbhpnppcggbcgedagnkighmdlei?hl=en).

### Modernizr

Modernizr functionality is provided in this boilerplate. Modernizr doesn't work inside the `Watch` script. Instead you need to manually set the tests you want to add inside the gulpfile then use the `Modernizr` script to run.

---

## **Asset Structure**

We take inspiration from the [SMACSS architecture](https://smacss.com/).

- **Base** - Base elements and utilities
- **Layout** - Spacing, major UI components, and layout structures
- **Modular** - All repeatable UI components
- **Tools** - Setup, Variables, Mixins, Fonts, Grid

---

## **Style Guide**

### Background

The styleguide we use is a custom, re-themed version of [Aigis](https://pxgrid.github.io/aigis/).

### Structure

The styleguide template structure loosely follows that of Brad Frost's [Pattern Lab](http://patternlab.io/about.html), in that we take inspiration for the following template levels:

- **Base** - This represents the atomic level (base styles)
- **Components** - This represents the modular UI components
- **Layout** - This represents structural framework components

### Usage

The styleguide is generated through comments in the `.scss` that follow a simple structure detailed below. The generation is on-the-fly through `npm run watch` or manual via `npm run styleguide`.

There is a boolean flag in the gulpfile incase you would rather not use the styleguide.

~~~
/*

---
name: Title Here
category:
 - Category
 - Category/Title
---

## Markdown description

Hello Component!

* Use the `.alt--class` modifier.

```html
<span>HTML Example</span>
<span class="alt--class">HTML Example</span>
```

*/
~~~
