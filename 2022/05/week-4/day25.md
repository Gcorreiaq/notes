# Scope
- [Redux](#redux)




# Redux

- **Store**: Instead of passing the state all the way down the components, we can use Redux to create a Store, where it will keep all the data our components need. This way we do not need to lift state up.\
\
Store is a globalized state.
```
let store = createStore(counter);
```
- **Action**: Actions are just a description of what is happening and what the application needs to do.
```
const increment = (n) =>
{
    return 
    {
        type: 'INCREMENT',
        payload: n
    }
}
```
- **Reducers**: Reducers transform the state into the next state, they change the data accordingly to the action.
```
const counter = (state = 0, action) =>
{
    switch (action.type)
    {
        case 'INCREMENT':
            return state + action.payloadj;
        default:
            return state;
    }
}
```
- **Dispatch**: The dispatch triggers the action to the reducer.
```
store.dispatch(increment(1));
```

- **combineReducers**: Use combineReducers to combine your reducers. \
Use import Reducers from './reducers', you do not need to specify index.js in the path.
```
[index.js]

import counterReducer from './counter.js'
import loginReducer from './login'

const Reducers = combineReducers(
{
    counter: counterReducer,
    isLogged: loginReducer
});
```

- **```<Provider>```**: To connect all your store to the app, wrap the App component with ```<Provider>```:
```
ReactDOM.render(
    <Provider store={store}>
        <App />
    </Provider>,
    document.getElementById("root")
);
```

- **useSelector()**: To access the data, import useSelector in your component:
```
import { useSelector, useDispatch } from 'react-redux'
import { increment } from './actions'
function App()
{
    const counter = useSelector(state => state.counter);
    const dispatch = useDispatch();
    return (
        <h1>{counter}</h1>
        <button onClick={() => dispatch(increment(1))}>+</button>
    );
}
```
