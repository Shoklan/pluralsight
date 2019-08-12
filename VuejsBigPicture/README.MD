# Vue.js: Big Picture
## Daniel Stern

# What is Vue.js?
- This course is to help you decide if you'd like to further your education.
- We're going to discuss what it is and whether it will help you with your business goals.
- We're going to discuss the core features of Vue.js.
- We're going to go over what specific challenges Vue.js was designed for.
- We're going to understand it better by comparing it to other popular JS frameworks.
- Then, pass along further resources to learn about Vue.js.
- E-commerce is moving in the direction of mobile phones:
![Native Apps vs Desktop/Mobile](images/e-commerce-transactions.png)
- Vue Apps can be built quickly; fast performance and small; build a view layer for app.
- What are the potential costs of using something else?:
  * Mobile users get bored due to slow load times.
  * Redrawing lists or updating the DOM is very slow.
  * Developers employed to update the application are slower and expensive to hire.
- So why Vue?:
  * It works for new or existing applications.
  * Replete with features familiar to those using React/Angular.
  * Feels simpler to understand and maintain.
  * Vue is popular.
- Who should use Vue?:
  * Small teams or individuals prototyping small apps.
  * Large teams collaborating can still find it useful; huge projects might not benifit.
  * Small contractors trying to update a legacy site.
    * You can *spot modify* sections of websites by filling it in with Vue.js
- Vue.js is a JavaScript library that is executed before your code to give it context.
- It is really JS code to build a **Render Engine** which is a kind of data model.
- It is a collaboration tool.
- What are the core features?:
  * Versatile Components.
  * It also has built-in Reactivity.
  * Fast initial load, fast render.
  * It comes with many directives.
- Vue files are appended with `.vue`
- These files are a conglomeration of HTML, CSS and JS code.
- These cannot be opened by web browsers.
- This means there is a build step to convert it from a `.vue`.
- This allows all the code for one component to be in a single file.
- These files have three sections:
  1. Template Section.
  2. Script Section.
  3. Style Section.
- The **Template** section contains HTML.
- The **Script** section contains application code.
- The **Styles** section contains the styles contained to this component.
- This is dependent on NPM to run.
- If you have it installed then you can install it using `npm install vue`.


# Why Use Vue.js
- What it does:
  * Output HTML Code for browsers.
  * Maps user interactions to JS methods you write.
  * Uses sophisticated techniques to speed up the rendering of applications.
  * Works in most browsers without any build step.
- What it doesn't do:
  * Create a server for your application.
  * Test your code for errors.
  * Significant Utility methods.
  * No routing.
  * No provided solution for modules beyond native ES6 support.
- **Reactivity** is the way in which applications change due to inputs from users or Servers.
- This is the principle problem Vue.js tries to solve.
- This is important because JS doesn't have built in reactivity.
![Developers vs Users](images/vue-reactivity-user-vs-Devs.png)
- A potential problem is that vue.js doesn't behave consistently with arrays and objects.
- There are techniques that have been developed to give the hint to vue.js to update.
- The element in the play application tags the div with `id="app"` which is where it will get dropped into.
- Where should you use Vue.js?:
  * Modernizing Legacy Applications.
  * Build Applications as a Team.
  * Prototyping.
- Vue.js can be included incrementally.
- It can co-exist with React/Angular without getting in the way.
- Benefits are felt immediately.
- So should you?:
  * Simple changes to the View Layer.
  * When new features are requested but are embedded in other code.
  * Application Code is ad-hoc.
- Where Vue.js shines is setting up and prototyping.
- And, there is very little difference between Vue.js prototypes and real Vue.js Apps.


# The Vue Ecosystem
- We're now be talking about libraries outside of Vue.js and have their own separate NPM install.
- To get the kind of functionality that comes with other libraries, you will require these.
- Here are some libraries and what they do:
  * **nuxt**: Universal Rendering.
  * **vuex**: State Management.
  * **vuetify**: Component Framework.
  * **vue-cli**: Scaffolding and Build.
- *Nuxt* is used to create universal Vue applications.
- While these are complicated - and we wont be covering them - these kinds of apps doe load faster.
- *Vuex* provides a way to update the state of your app.
- It's used to keep applications with massive state manageable.
- *Vuetify* contains sleep and performant Vue Components.
- You would use this if you were creating your own solution for UI.
- *Vue-cli* is a tool for creating, building and updating Vue Applications.
- Some example commands:
  * `vue serve`: Server the application to your browser.
  * `vue build`: Converts the .vue files and converts them to JS,HTML.
  * `vue create`: Creates a new Vue project.
  * `vue ui`:  Creates a new Vue project.
  * `vue add`: installs plugins for Vue-cli
![File Size - Minimized of Comparable Frameworks](images/)
- There are some pitfalls to the framework.
  * Needs support from ecosystem.
  * Tricky reactivity.
  * .vue may confuse new devs.
  * It's new and untested in some untested areas.


# Reference:
- [Vue.js Github Page](https://github.com/vuejs/vue)
- [Vue.js Documentation](https://vuejs.org)
- 


# Research:
- Flux?
- Redux?
