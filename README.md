# imoney-react-switch
![-1](https://cloud.githubusercontent.com/assets/1193966/25661681/26387524-3044-11e7-96db-dcab1fd9e061.png)

## Browser support

IE9+
## Installation

    npm i imoney-react-switch

## Usage

```js
import React from 'react';
import ReactDOM from 'react-dom';
import Switch from "imoney-react-switch";
import "imoney-react-switch/src/index.css";
```

```js
class App extends React.Component {
    constructor(props) {
        super(props);
        this.state = {
            checked: true
        };
        this.changeState = this.changeState.bind(this);
    }

    changeState(e, checked) {
        e.stopPropagation();
        this.setState({
            checked: checked
        });
    }

    render() {
        return (
            <div>
                <Switch onChange={this.changeState} checked={this.state.checked}/>
            </div>
        );
    }
}
ReactDOM.render(
    <App />,
    document.getElementById('app')
);
```
### index
```js
changeState(e,checked,index){
    e.stopPropagation();
    console.log(index);
},
```
```js
<Switch index="1" onChange={this.changeState} checked={true}/>
<Switch index="2" onChange={this.changeState} checked={true}/>
```
### disable
```js
<Switch disable={true} onChange={this.changeState} checked={true}/>
```

