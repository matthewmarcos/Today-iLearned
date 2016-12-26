# Reactjs

### What is Reactjs?
React js is a view library that is used to render things on the client.
It is used to render a page depending on a state.
The state is can be managed by another library like Redux.

### Thinking in React
The fundamental unit of a webpage is called a component.
A component may be a widget, a button, or an element that sits in the DOM.
It may or may not be aware of its neighboring components.
A component can have subcomponents, called *children*.


### Writing React
React is written in a different syntax called jsx.
It is usually written in a .jsx file, but can also be written in .js files depending on your webpack loader.
Because web browsers (As if December, 2016) only understand HTML, CSS, and Javascript, a developer writing in jsx needs to *transpile* his jsx code into browser readable javascript or html. We use webpack for this. Webpack can watch for changes in the react code, then on every change, retranspiles the jsx into javascript/css code, rebundles it, and places it in a destination folder accessible by the client (usually public).

Because the javascript bundle changes, it may be a good idea to use *hot reloading*. It is the process of automatically refreshing the client browser everytime a new bundle is served. We used to do this with browserSync with a gulp task. In webpack, we use the `--inline` flag

Because webpack is pro and React is component based, the nerds in Webpack have introduced HMR or Hot Module replacement, where only the component that has changed on the client will be 're-rendered'. This is done with the `--hot` flag when starting webpack.

