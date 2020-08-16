## Some Commonly used React Patterns?

These are some of the commonly used react patterns:

1.__Element__
    
 * Elements are anything inside angle brackets.

```js
<div></div>
<App />
```
   * Components return elements. 

2.__Component__ 

   *  These are nothing but functions which return a React Element

```js
function App(){
    return  <h1> Hello World!!!</h1>
}
``` 

3.__Expressions__

   * use curly braces to embed expression in JSX

```js
function Greeting() {
  let name = "sridhar";

  return <div>Hi {name}!</div>;
}
```
4.__defaultProps__
   * Specify default values for props with __defaultProps__.

```js
function App(props) {
  return <div>Hi {props.name}!</div>;
}
App.defaultProps = {
  name: "Guest"
};
```
5.__Destructuring Props__

   * Destructuring is an ES6 feature which will be used commonly in react used to destructure objects and arrays.

```js
let person = { name: "sridhar"}
let { name} = person

``` 
   * Similarly, we can destructure Arrays

```js
let things = ["one", "two"];
let [first, second] = things;
```
 
   * Destructuring is used a lot in functional components. These component declarations are as below

```js
function Greeting(props) {
  return <div>Hi {props.name}!</div>;
}

function Greeting({ name }) {
  return <div>Hi {name}!</div>;
}

```
 * There's is a syntax for collecting props into an object. It is [react parameter syntax](https://developer.mozilla.org/en- 
   US/docs/Web/JavaScript/Reference/Functions/rest_parameters) and it looks like this

```js
function Greeting({ name, ...restProps }) {
  return <div>Hi {name}!</div>;
}

```
 * Those three dots (...) take all the remaining properties and assign them to the object restProps.

6.__Conditional rendering__ 

  * You can't use if/else statements inside component declarations. So conditional (ternary) operator and short-circuit evaluation are your friends.

 __If__

```
{
  condition && <span>Rendered when `truthy`</span>;
}
```

 __unless__

```
{
  condition || <span>Rendered when `falsy`</span>;
}
```

__if-else__

```
{
  condition ? (
    <span>Rendered when `truthy`</span>
  ) : (
    <span>Rendered when `falsy`</span>
  );
}
```

>If you have any doubts related to this article or anything related to tech or software-engineering in general, drop a comment here or you can message me on twitter [@ksridhar02](https://twitter.com/ksridhar02).

