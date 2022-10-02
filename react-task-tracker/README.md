# `Assignment 1`
# `Student Id: 2030407`

## `What is React?`
    React is a JavaScript library for building reusable interfaces. React was created by Facebook, initially released on May 29, 2013. React has its own virtual DOM to make new changes and it updates only the elements which needs to be changed.

    React latest version is 16.13.1. React run on the client as Single Page App. React is often referred to as the front-end framework, because it is capable and directly comparable to a framework such as Angular or Vue.

## `Why React?`

    - It gives structure to a view layer (User Interface) of an application.
    - React allows to build UI with the reusable components, so every part of the UI can be looked as the dynamic components which can hold its own state and logic.
    - Since React uses JSX, we don’t need to separate markup from logic, this allows us to write dynamic HTML, we can embed javascript expressions, variables,etc.
    - The apps build with React are very interactive because it uses its own virtual DOM (Document Object Model), which allows us to update parts of the page without reloading, which makes it more interactive and dynamic to use.
    - React also has performance and testing benefits.
    - It is very big in the industry right now, as it manages data very easily, with data binding. It helps with debugging with better performance. 

## `Components:` 
    Components are independent and reusable bits of code. They serve the same purpose as JavaScript functions. There are two types of components: 
        - Function Components: A React functional component is a simple JavaScript function that accepts props and returns a React element. After the introduction of React Hooks, writing functional components has become the ​standard way of writing React components in modern applications.
        - Class Components: These components are simple classes (made up of multiple functions that add functionality to the application)
    Components can have state which is an object that determines how a components renders or behave.

## `Hooks:`
    React Hooks are simple JavaScript functions that we can use to isolate the reusable part from a functional component. Hooks can be stateful and can manage side-effects.
    1) useState: To manage states. Returns a stateful value and an updater function to update it.
    2) useEffect: To manage side-effects like API calls, subscriptions, timers, mutations, and more.

## `To start a React application: We use npm (node packet manager),` 

## `Install nodejs`
React dev tools (add browser extension).
( to setup all the files and folders, packages, etc.)
```
    npx create-react-app my-app 
```
```
    cd my-app
```
(To start the dev server: for ex: (http://localhost:3000)
```
    npm start 
```
In React we cannot change the state, else we use useState to change any objects.
To install icons in React, we use:
```
    npm i react-icons
```
`For production:`

To build for production: npm run build, it creates “build” folder which is used to deploy.
To push the build folder locally we use: 
(for mac/linux),
```
    sudo npm i -g serve  
```
it is basically a http server.
To serve build folder on any port: 
```
    serve -s build -p 8000  (http://localhost:8000)
```

`To deal with Back-end :`

We use JSON server to create a mock rest API, to use our own data.
```
    npm i json-server 
```
To run this, we add a script to the package.json folder called,
"server": "json-server --watch db.json --port 3000"

```
    npm run server (which creates db.json)
```
Again we run our dev server with - 
```
    npm start
```
Then after creating the database in the db.json by adding json objects, we run
- to fetch task from backend: http://localhost:3000/tasks

## `We use a hook called “useEffect” to load effects on the page loads.`

To delete data from the server : 

We use method: ‘DELETE’
```
    const deleteTask = async (id) => {
     await fetch(`http://localhost:3000/tasks/${id}`,{
       method: 'DELETE'
     })
    
     setTasks(tasks.filter((task)=> task.id !== id))
    }
```

To Add data :

We use method: ‘POST’
```
    const addTask = async (task) => {
     const res = await fetch('http://localhost:3000/tasks',{
       method: 'POST',
       headers: {
         'Content-type': 'application/json'
       },
       body: JSON.stringify(task)
     })
    
     const data = await res.json()
    
     setTasks([...tasks, data])
    }
```







# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
