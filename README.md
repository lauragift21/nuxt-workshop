<h1 align="center">
Building From Scratch with Nuxt Workshop
</h1>

<p align="center">This workshop is for anyone with knowledge of JavaScript and Vue.js interested in building web applications with Nuxt.js</p>

Instructor: <a href="https://giftegwuenu.com">Gift Egwuenu</a>

[Workshop Slides](https://miro.com/app/board/o9J_kki51ks=/)

## Sections
- [Introduction](#Introduction)
- [Setup and Installation](#setup-and-installation)
- [What is Nuxt.js and what does it offers](#what-is-nuxt.js-and-what-does-it-offers)
- [A Look at the Nuxt Directory Structure](#a-look-at-the-nuxt-directory-structure)
- [Configuring Nuxt with Nuxt.config.js](#configuring-nuxt-with-nuxt-config-js)
- [The concept of Layout and Pages](#the-concept-of-layout-and-pages)
- [File System Routing with Nuxt](#file-system-routing-with-nuxt)
- [Fetching Data in Nuxt.js](#fetching-data-in-nuxt-js)
- [Improving SEO with vue-meta](#improving-seo-with-vue-meta)
- [Nuxt Plugins](#nuxt-plugins)
- [Managing state with Vuex Store](#managing-state-with-vuex-store)
- [Extending the app with Nuxt Modules](#extending-the-app-with-nuxt-modules)
- [Deploying the App to Netlify](#deploying-the-app-to-netlify)


## Introduction
[Nuxt.js](https://nuxtjs.org/) is a Vue framework for creating modern web applications that makes development painless and powerful with great developer experience.

In this workshop, we'll cover everything you need to know to build a web application from scratch with Nuxtjs. Some things we'll cover include setting up a nuxt app and extending it's functionality with Nuxt Modules and finally, we'll look at some deployment strategies.

## Setup and Installation
You need to have [Node](https://nodejs.org/) installed on your computer before we begin the workshop.

Download Node for windows [here](https://nodejs.org/en/download/)

Download Node for Mac using [Homebrew](https://brew.sh/).

If you don't have that installed use this command to install it

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

```
and then install node:

```bash
brew install node
```

### Install Nuxt with Create Nuxt App

```bash
npx create-nuxt-app <project-name>
```

We already have a repo setup so go ahead and clone this repo using the following commands:

```
git clone https://github.com/lauragift21/nuxt-workshop.git
```

```
cd nuxt-workshop && yarn
```

This repo is setup to use [TailwindCSS](https://tailwindcss.com/) for styling*

## What is Nuxt.js and what does it offers?

[Nuxt.js](https://nuxtjs.org/) is an open-source Vue framework for building modern web applications that makes development painless and powerful with a great developer experience.

Some of these features are what make Nuxt performant and a good choice for your app:

* Automatic Code Splitting
* Server-Side Rendered, Static-Site Generated / Jamstack, SPA
* Powerful routing system with asynchronous data
* Extend with modular architecture
* Hot Module Replacement in Development
* Write Vue Files **(*.vue)**
* ES6 Transpilation
* Powerful Lighthouse scores out of the box!
* Pre-processing - SCSS, SASS, LESS.

## A Look at Nuxt Directory Structure

The default Nuxt application structure is made up of different files and directories in itself which can be used for building small or large scale application. The way the directory is setup can always be changed to fit your project needs.

```bash
.
├── assets
│   └── README.md
├── components
│   ├── AppNav.vue
│   ├── Logo.vue
│   └── README.md
├── layouts
│   ├── default.vue
│   └── README.md
├── middleware
│   └── README.md
├── pages
│   ├── index.vue
│   └── README.md
├── plugins
│   └── README.md
├── static
│   ├── favicon.ico
│   └── README.md
├── store
│   └── README.md
├── .gitignore
├── nuxt.config.js
├── package.json
└── README.md
```

## Configuring Nuxt with `nuxt.config.js`

The configuration for Nuxt application is great and it already covers most use-cases, but Nuxt allows you extend the configuration by specifying the config properties in the `nuxt.config.js` file.

Nuxt let's you customise **webpack configuration**,  define **CSS libraries** to use globally, create environment variables, define meta data for your application and so much more can be done in the config file.

## The Concept of Layout and Pages

## File System Routing in Nuxt.js

## Fetching Data in Nuxt.js

## Improving SEO with Vue-Meta

In Nuxt applications, we can significantly improve SEO of the pages by adding correct meta tags to respective pages. Nuxt uses Vue Meta under the hood to update the document head and meta attributes of your application.

You can add meta information in three different ways in Nuxt.js:

![SEO Slide](./static/Seo.jpg)

* Globally using the `head` property in nuxt.config.js

```js
export default {
  head: {
    title: 'Nuxt Workshop',
    meta: [
      { charset: 'utf-8' },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        hid: 'description',
        name: 'description',
        content: 'This is the Nuxt Workshop Site'
      }
    ],
    link: [{ rel: 'icon', type: 'image/x-icon', href: '/favicon.ico' }]
  }
}
```

* Locally using the `head` as an object

```js
<script>
export default {
  head: {
    title: 'About',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'This is the about page'
      }
    ],
  }
}
</script>
```
* Locally using the `head` as a function so that you have access to data and computed properties.


```js
<script>
export default {
  data () {
    return {
      title: 'About'
    }
  },
  head() {
    return {
      title: this.title,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'This is the about page'
        }
      ],
    }
  }
}
</script>
```

## Nuxt Plugins

## Managing state with Vuex Store

## Extending the app with Nuxt Modules

## Deploying the app to Netlify

## Additional Resources 
[Nuxt Documentation](https://nuxtjs.org/guides)  
[Nuxt Content](https://content.nuxtjs.org)  
[Tailwind CSS](https://tailwindcss.com)

## License

[![Creative Commons License](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/)

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/)