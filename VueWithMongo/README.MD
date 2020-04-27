# Building Business Applications with Vue.js and MongoDB
## Mark Scott

# Get Introduction to the Course
- Vue.js is growing in the Application world.
- We're going to go over how to build an application with Vue.js and MongoDB.


# Technology Stack Overview
- If you're looking to be a full stack JS developer and looking for a tech stack then welcome.
- This course will introduce you to the **Venom Stack** for Application Development.
![Venom Stack](images/venom-stack.png)
- We're going to be working on a minimally viable application for a client.
- We're building a basic banking interface.
- We're start with an Architectural Approach to the project.
- The parts are:
  1. UI Layer.
  2. RESTful API.
  3. Data Access.
- *Separation of Concerns* is important for tech swapping.
![Site Roadmap](images/site-roadmap.png)
- The Core of the framework is Node.js.
- The API layer will be Express.js
- The UI Layer will be managed by Vue.js
- The connection to the Database can be managed by the app or by something design explicitly for that management: **Mongoose**.
- It might be worth watching the other courses about Mongoose to help out.
- Having data is of no use if you cannot access or use it.
![API Overview](images/api-overview.png)
- We'll be using **Material Design Principles** from the the Material Design Project.
- Those principles are:
  1. Material is the metaphor.
  2. Bold, Graphic, Intentional.
  3. Motion provides meaning.
![ Material Design Principles](images/material-principles.png)
- From that project, we'll be using *Vuetify* from this project.
- This supplies us with lots of attractive assets for UI usage.
- We'll be using a few other npm packages as well:
![Packages to Install](images/packages-to-install.png)
![More Packages](images/more-packages.png)
![Even More Packages](images/even-more-packages.png)
- We'll be using the **Postman** program to test our APIs.
- We could develop our MongoDB database via the Comamnd line but we're going to use a different tool instead called Studio 3T.
- The Free version would be Robo 3T instead.


# Setting Up the Demo Applications
- Now we'll be builing and installing everything.
- Install nodejs
- We'll also need to install yarn from [yarn's website](yarnpkg.com)
```bash
npm install -g vue-cli
```
- Then we'll create the project in the correct directory:
```bash
vue init webpack client
# vue initialize <template> <project-name>
```
- This will give you a few fields to fill out.
- Then you change to the correct directory; the start with:
```bash
npm run dev
```
- Normally, you will have a different server for the API and the database:
![Baseline Architecture](images/base-arch.png)
- We're going to use separate folders to simulate this.
- After getting the project folder loaded, we'll start working in main.js


# Designing the Data Layer with MongoDB and Mongoose
- We should ask ourselves whether the data or the design matters more to the users.
- In our case, we'll work on the Data layer first.
- Once you're ready, navigate to [Install MondoDB](docs.mongodb.com/manual/installation/) to install MongoDB for your OS.
- Download and install Robo 3T and create collections **users** and **transactions**.
- **"Everything in Mongoose starts with a schema"**.
- Here is the schema we'll be using:
![Schema Example](images/schema-example.png)
- Here are the Mongoose Schema Types:
![Mongoose Schema Types](images/mongoose-schema-types.png)
- Calling `npm init -f` will force it to use the default settings and not ask for anything.
- We'll want auto-reload on changes and *nodemon* is a popular choice.
- You can install it using `npm install nodemon -g`.
- Now we'll define our models in the `models` folder in our **server** folder project.
```js
const mongoose = require('mongoose')
const Schema = mongoose.Schema

let userSchema = new Schema({
  first: { type: String, required: true },
  last:  { type: String, required: true },
  email: { type: String, required: true },
  password: { type: String, required: true },
  isActive: { type: Bool, default: true },
  createdOn: { type: Date, default: Date.now }
})

const User = mongoose.model('User', userSchema)
modeule.exports = User
```
- We're doing the same thing for transactions:
```js
const mongoose = require('mongoose')
const Schema = mongoose.Schema

let transactionSchema = new Schema({
  userId: mongoose.SchemaTypes.ObjectId,
  transactionDate:  { type: Date, required: true },
  transactionType:  { type: String, required: true },
  description: { type: String, required: true },
  charge:  { type: Number, default: 0 },
  deposit: { type: Number, default: 0 },
  notes:   { type: String, default: '' },
  createdOn:   { type: Data, default: Date.now },
})

const Transaction = mongoose.model('Transaction', transactionSchema)
modeule.exports = Transaction
```


# Developing the API with Node and Express

# UI Development with Vue.js and Vuetify

# Manage Application State with Vuex

# Getting Data from the API

# Finalizing the Demo Application

# Summary:

# Research:
- [Material Design Website?](materials.io)

# Reference:
