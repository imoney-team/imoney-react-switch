# imoney-react-swtich

## Browser support

IE9+

## Usage

```js
import React from 'react';
import ReactDOM from 'react-dom';
import Switch from "imoney-react-swtich";
import "imoney-react-swtich/src/index.css";
```

```js
let App = React.createClass({
    changeState(e,checked){
        e.stopPropagation();
    },
    render () {
        return (
            <div>
                <Switch onChange={this.changeState} checked={true}/>
            </div>
        )
    }
});
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

