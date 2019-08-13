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


# Creating Vue.js Templates
- Templates are created as HTML.
- The data property servers two purposes:
  1. At design time, it represents the schema.
  2. At runtime, servers as the model.
- **Plain Old Javascipt Object (POJO)**
- Vue makes shortcuts to the data properties for you to access.
- When initialized, the `Object.defineProperty` function sets up the getters and setters of the object.
- You can only modify properties that exists once declared.
- You cannot add or remove them either.
- Due to this, objects don't lookin like normal API calls:
![Examples of Normal API call Vs Vue](images/api-expected-vs-normal.png)
- Naming rules are:
  * Letters, digits, dollar signs, underscores.
  * Must start with a letter.
  * Case sensitive
  * Cannot use reserved words.
- One specific rule only for Vue is that properties should not start with $ or _
- The value of the property is what will show in the Vue.
- **Data Properties should just be data!**.
- Vue accepts primitive types but ignores other not native object types.
- Example being: Number, String, Date, Array
- Vue has two ways to bind text to a view:
  * Semantic Syntax with `{{ }}`; also called moustaches.
    * If the value does not exist, then it will replace it with an empty string.
  * Declarative Bindings are created via directives.
    * All baked in directives start with `v-`.
    * Another example would be `v-text="appName"` which will do the same thing.
    * If you need to bind to only part of an element then use semantic syntax.
    * The directive `v-once` will only allow an element to change once and never again.
    * Keep in mind that the children of an element with this directive will inherit it as well.
    * You can pass raw html but you will need to use the `v-html` directive otherwise it shows as raw text.
    * Note that you cannot nest bindings.
    * Only bind to HTML you trust.
    * Don't bind to User Generated HTML.
- The directive `v-bind` is for binding to HTML attributes.
- This allows you to bind data property values to HTML attributes.
- This would look like `v-bind:src="appLogo"` but can also look like `:src="appLogo"`.
- While you should keep your design separate from your logic, sometimes it's unavoidable.
- When you have to, you'll need to choose between getting it from a JS object of a JS array.
```
v-bind:style="{ color:color }"
```
- If you need to change properties with - in them then you can use Camel Case and it will still work.
```
fontFAmily:appNameFontFamily
```
- You can refactor all the changes that you'd want to make and include them on the data side and load them with `v-bind:"appStyle"`.
- You might have seen something like this before:
```js
var isLocal = location.host.includes('localhost'):
```
- An **Expression** is a type of **Statement**.
- An *Expression* is defined as a line of code that produces a value.
- Bindings can only be expressions.
- For example, this code will change passed on whether something is online or offline:
![Bindings Expression Example](images\bindings-expression-example.png)
- *Expressions* run within a sandbox.
- The total list of white listed items is:
![Whitelisted JS for Sandbox](images\bindings-whitelist.png)
- Global that are white listed cannot be used in Vue Expressions.
- This includes Jquery $.


# Binding with Forms in Vue.js
- The main way to collect data through the web is via forms.
- Two way bindings can be created using the `v-model` directive.
- A *Text Field* is usually created with two tags: input and textarea.
- Vue has support for the following Text Inputs:
![Textual Input Types Supported](images\supported-text-inputs.png)
- Vue does not support using mustaches for binding in a textarea.
- Binding to a checkbox is basically the same except you need to set the type to checkbox.
- However, binding to multiple values is tricky and you'd want to add the values to an array.
- Drop downs can be created using a select element.
- By default, Vue syncs the data whenever a input event is fired.
- Once it fires, the input can go through several modifiers:
  * Trim string values.
  * Convert input values to numbers.
- The `trim` modifier will remove leading and trailing whitespace, tabs and linebreaks.
- If you want it to be run, then you append it: `v-model.trim`.
- The `number` modifier will try and convert user input into a number.
- If you want it to be run, then you append it: `v-model.number`.
- The onchange event is different since it only fires after the element has lost focus.
- If you want this feature then you'll append it `v-model.lazy`.


# Responding to User Events in Vue.js

# Conditional Rendering and Rendering of Lists

# Reading to Data Changes with Filters, Computed Properties and Watchers

# Reference:
- [Courses Github Repo](https://github.com/efofic/course-vue-getting-started)
-


# Research:
- Snapdom?
