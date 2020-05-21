# How State is Set
Earlier in this lesson, we saw how we can define a component's state at the time of initialization. Since state reflects mutable information that ultimately affects rendered output, a component may also update its state throughout its lifecycle using `this.setState()`. As we've learned, every time local state changes, React will trigger a re-render of the component by calling its `render()` method.

There are two ways to use `setState()`. The first is to merge state updates. Consider a snippet of the following component:

``` javascript
class Email extends React.Component {
  state = {
    subject: '',
    message: ''
  }
  // ...
});
```

Though the initial state of this component contains two properties (`subject` and `message`), they can be updated independently. For example:

``` javascript
this.setState({
  subject: 'Hello! This is a new subject'
})
```

This way, we can leave `this.state.message` as-is, but replace `this.state.subject` with a new value.

The second way we can use `setState()` is by passing in a function rather than an object. For example:

``` javascript
this.setState((prevState) => ({
  count: prevState.count + 1
}))
```

Here, the function passed in takes a single `prevState` argument. When a component's new state depends on the previous state (i.e., we are incrementing `count` in the previous state by 1), we want to use the functional `setState()`.





#CodeCademy Learn React/07 - State#