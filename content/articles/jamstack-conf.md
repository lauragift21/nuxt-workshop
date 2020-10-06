---
title: Jamstack Conf Workshop
description: A summary of my experience at Jamstack Workshop
img: https://images.unsplash.com/photo-1468577760773-139c2f1c335f?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&h=300&q=80
alt: jam bread
tag: recap
author: 
  name: Jones Doe
  bio: Software Developer
  image: https://images.unsplash.com/photo-1509460913899-515f1df34fea?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=934&q=80
---

# Jamstack Conf Workshop

Building from Scratch with Nuxt.js


#### Inject variable in \$root or context

When there's a need to make functions or values available across the app. We can inject those variables into **Vue instances (client side)**, the **context (server side)** and even in the Vuex store. It is a convention to prefix those functions with a $.

## Managing state with Vuex Store

## Extending the app with Nuxt Modules

Modules are Nuxt.js extensions which can extend its core functionality and add endless integrations.

[A list of curated Modules from the Nuxt Community](https://github.com/nuxt-community/awesome-nuxt#modules)

In our app, we're already using a TailwindCSS Module as a `buildmodule` - that are only imported during build time or in development mode.