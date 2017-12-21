# React
- **[Components](#components)**
- **[Props](#props)**
- **[State](#state)**
- **[Lifecycle](#lifecycle)**
---


## Components
**Function components**

- don’t have state
- don’t have life cycle methods
- don’t have a this

```javascript
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```
**Class components**

```javascript
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```
## Props
```javascript
class Welcome extends React.Component {
  render() {
    return <h1>Hello {this.props.name}</h1>;
  }
}

function Welcome(props) {
  return <h1>Hello {props.name}</h1>;
}

const element = <Welcome name="Sara" />;
```
*Default props*
```javascript
class Welcome extends React.Component {
  render() {
    return <h1>Hello {this.props.name}</h1>;
  }
}

Welcome.defaultProps = {
  name: "world",
};
```
## State
***state is created in the component***
```javascript
constructor() {
  super();
  this.state = {
    count: 0,
  };
}
```
***state is changeable***
```javascript
updateCount() {
  this.setState((prevState, props) => {
    return { count: prevState.count + 1 }
  });
}
```
## Lifecycle
**Mount**

- ***constructor()***
- *componentWillMount()*
- ***render()***
- *componentDidMount()*

**Update**

- *componentWillReceiveProps()*
- *shouldComponentUpdate()*
- *componentWillUpdate()*
- ***render()***
- *componentDidUpdate()*

**Unmount**

- *componentWillUnmount()*