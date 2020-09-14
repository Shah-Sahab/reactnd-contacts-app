
# Notes
#### This helps in explaining what libs used in the project and any Reading Materials associated with it.

## Type checking a Component's Props with PropTypes

As we implement additional features into our app, we may soon find ourselves debugging our components more frequently. For example, what if the props that we pass to our components end up being an unintended data type (e.g. an object instead of an array)? PropTypes is a package that lets us define the data type we want to see right from the get-go and warn us during development if the prop that's passed to the component doesn't match what is expected.

To use PropTypes in our app, we need to install prop-types(https://facebook.github.io/react/docs/typechecking-with-proptypes.html):

npm install --save prop-types

Alternatively, if you have been using yarn(https://www.npmjs.com/package/yarn) to manage packages, feel free to use it as well to install:

yarn add prop-types


## PropTypes Recap

All in all, PropTypes is a great way to validate intended data types in our React app. Type checking our data with PropTypes helps us identify these bugs during development to ensure a smooth experience for our app's users.
Further Research

    prop-types library from npm - https://www.npmjs.com/package/prop-types
    Typechecking With Proptypes from the React Docs - https://facebook.github.io/react/docs/typechecking-with-proptypes.html



escape-string-regexp - https://www.npmjs.com/package/escape-string-regexp
sort-by - https://www.npmjs.com/package/sort-by

## Controlled Components Recap

Controlled components refer to components that render a form, but the "source of truth" for that form state lives inside of the component state rather than inside of the DOM. The benefits of Controlled Components are:

    instant input validation
    conditionally disable/enable buttons
    enforce input formats

In our ListContacts component, not only does the component render a form, but it also controls what happens in that form based on user input. In this case, event handlers update the component's state with the user's search query. And as we've learned: any changes to React state will cause a re-render on the page, effectively displaying our live search results.


## Putting it All Into Perspective

When it comes to keeping track of data in your app, think about what will be done with that data, and what that data will look like as your user interfaces with your app. If you want your component to store mutable local data, consider using state to hold this information. Many times, it is state that will be used to manage controlled form elements in your components.

On the other hand, if some information isn't expected to change over time, and is generally designed to be "read-only" throughout your app, consider using props instead. Both state and props will generally be in the form of an object, and changes in either will trigger a re-render of the component, but they each play very different roles in your app.

We covered a lot in this lesson, and you've made great progress - great work!

## Lesson Challenge

Read these articles: Thinking in React (https://facebook.github.io/react/docs/thinking-in-react.html), Functional Components vs. Stateless Functional Components vs. Stateless Components (https://tylermcginnis.com/functional-components-vs-stateless-functional-components-vs-stateless-components/), Controlled Components (https://facebook.github.io/react/docs/forms.html) , Avoiding React SetState() Pitfalls (https://www.duncanleung.com/blog/2017-07-15-avoiding-react-setstate-pitfalls/), and How to NOT React: Common Anti-Patterns and Gotchas in React(https://codeburst.io/how-to-not-react-common-anti-patterns-and-gotchas-in-react-40141fe0dcd) . Answer the following questions and share your answers with your Study Group.

1) What is the difference between Stateless Functional Components and class components?

2) Describe the reasoning behind Controlled Components.

3) What is the correct way to modify state? Make sure to explain what role a child component like “Add User” can have in the app.


## componentDidMount() Recap

componentDidMount() is one of a number of lifecycle events that React offers. componentDidMount() gets called after the component is "mounted" (which means after it is rendered). If you need to dynamically fetch data or run an Ajax request, you should do it in componentDidMount().
Further Research

    componentDidMount(https://facebook.github.io/react/docs/react-component.html#componentdidmount) from the React Docs

