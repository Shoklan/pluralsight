# Vue.js Fundamentals
## Jim Cooper

# Getting Started with the Vue.js CLI
- We're going to build a Build-a-Bot Website.
- A **Vue Instance** is called whenever you call `new Vue()`.
- In a typical Vue application, you'll only have one Vue Instance.
- If you're familiar with React or Angular, then you'll be familiar with the Components and sub-components of Vue.
- You'll also have **Router Views** which will change based on what the contents are.
- So, we'e going to work on creating this from the ground up.
- We're going to need some tools:
  * git
  * node.js
- We create a project with `vue create build-a-bot` with the CLU interface.
- Much of this has come as of version *3.x* of the Vue CLI.
- Another person that recommends Visual Studio Code.
- You can run the created project using `npm run serve`.
- Right now, there is only the render function in the file:
```js
import Vue from 'vue';
import App from './App.vue';

new Vue({
  render: h => h(App),
}).$mount('#app');

```
- When you look at the App.vue file, it's clear a browser cannot read this.
- There is a component of Vue that will read and compile it into a format they can use.


# Creating Vue.js Components and Using Template Syntax
- 



# Routing from Page to Page

# Managing State and Server Communication with Vuex

# Creating Custom Directives and Filters

# Deploying Vue Applications to Production

# Reference:

# Research:
