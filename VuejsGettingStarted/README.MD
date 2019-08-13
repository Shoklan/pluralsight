# Vue.js: Getting Started
## Chad Campbell

# Introduction to Vue.js
- Vue.js is an intuitive Framework for building Web Apps.
- It has a focus on speed and simplicity.
- "Complexity can make an app error prone and difficult to maintain."
- **Templates** separate the UI from the Data and Business Logic.
- Exmaple;
![Showing of Separation of UI and Data/Logic](images/template-visual-break.png)
- *Templates* minimize how much code you have to write.
- They also protect you from changes.
- **Declarative Bindings** are the glue that holds the UI and data together.
- From a Runtime perspective, changing the DOM is expensive.
- This is because the browser has to recalculate everything in the window.
- The **Virtual DOM** is like a lightweight copy of the actual DOM.
- It efficiently determines what needs to be updated and batches those updates.
- Two other concerns to bring up will be Browser support and licensing.
![Browsers Supported](images//browswer-support-blocks.png)
- The maintainers of Vue.js has stated that the CDN unpkg is the most well synced source for including.
- Always include the url source as `https://unpkg.com/vue` which redirects to the latest version of Vue.js
- If you want to specify the version, then you can use `https://unpkg.com/vue@<version>/dist/vue.min.js`
- Include it at the bottom of the page and ours will looks like:
```
<script
  type="text/javascript"
  src="https://unpkg.com/vue@2.2.5/dist/vue.min.js"
</script>
```
- The library **Axios** is the recommended way to make HTTP requests.
- The script block is the same but just points to `.../axios/.../axois.min.js` instead.
- To initialize an instance of Vue,
- This is how you initialize the app on the Data side:
```vuejs
var growler = new Vue({
  el: '#growler',
  data: { }
});
```
- **Mounting** is when you make the view becomes visible to the user.
- The tag `el` specifies where it will be mounted onto into the webpage.
- You can use a CSS Selecter `'#growler'` or using the longer version `docuemnt.getElementByID('growler')`
- This will replace the element in the page with the View generated.
- Due to this, **do not set it to body or html elements**.
- Each View has a lifecycle.
- They are:
  1. Creation.
  2. Mounting.
  3. Updating.
  4. Destroy.
- Each hook for each stage is named:
  * `before<State>`, `<state>ed`
- The creation state starts when you call the `Vue()` constructor.
![Vue Lifecycle](images/lifecycle-overview.png)
- Note that you must call the destroy instance explicitly otherwise it will not run.
- 


# Creating Vue.js Templates

# Binding with Forms in Vue.js

# Responding to User Events in Vue.js

# Conditional Rendering and Rendering of Lists

# Reading to Data Changes with Filters, Computed Properties and Watchers

# Reference:
- [Courses Github Repo](https://github.com/efofic/course-vue-getting-started)
-


# Research:
- Snapdom?
