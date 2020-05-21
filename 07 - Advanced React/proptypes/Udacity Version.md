# Udacity Version
Type checking a Component's Props with PropTypes
As we implement additional features into our app, we may soon find ourselves debugging our components more frequently. For example, what if the props that we pass to our components end up being an unintended data type (e.g. an object instead of an array)? PropTypes is a package that lets us define the data type we want to see right from the get-go and warn us during development if the prop that's passed to the component doesn't match what is expected.

To use `PropTypes` in our app, we need to install `prop-types`:

`npm install --save prop-types`

``` javascript
import PropTypes from 'prop-types';

class Email extends React.Component {
  render() {
    return (
      <h3>Message: {this.props.text}</h3>
    );
  }
}

Email.propTypes = {
  text: PropTypes.string.isRequired
};
```

#CodeCademy Learn React/09 - Advanced React/PROPTYPES#