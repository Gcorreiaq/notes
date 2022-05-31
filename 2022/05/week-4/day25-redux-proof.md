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

# Proofs

- **Proof of statements containing a existential quantifier (∃x ∈ U )(P(x))**: There are two ways to prove this, by a constructive proof or by a non constructive proof. \
\
**Constructive proofs**: We show a specific element of the universe of discourse which makes P(x) true. \
_For example, to prove the theorem "There exists an even prime" all we need to do is to note that the natural number 2 is even and it is divisible by 1 and itself only. Thus, by exhibiting the even, prime, natural number 2, we have given a constructive proof of the statement "There exists an even prime"_. \
\
**Nonconstructive proofs**: In nonconstructive proofs, we do not show a specific element in the universal set, we use other theorems that prove the existence of a element. \
\
_A nonconstructive proof of the statement "There is a real solution of the equation x^3 - 2x + 5 = 0" proceeds as follows: Let p(x) = x^3 - 2x + 5, the p(x) is of degree 3 and has real coefficients. By the Fundamental Theorem of Algebra, the polynomial p(x) has exactly 3 solutions. By the Conjugate Root Theorem p(x) = 0 has an even number of complex roots -- either 2 or 0. Hence, the equation p(x) = 0 must have 1 or 3 real roots._ \
\
**Fundamental Theorem of Algebra**: “If p(x) is a polynomial of degree n ≥ 1 with complex coefficients, then there exist n solutions of the equation p(x) = 0.” \
\
**Conjugate Root Theorem**: "If p(x) is a polynomial of degree n ≥ 2 with real coefficients, then if a + bi where b != 0 is a solution of the equation p(x) = 0, then a − bi is a solution also". \
\
**Uniqueness Theorem**: A theorem which states that there is one and only one element in a specific set which satisfies a certain statement is called a uniqueness theorem. Often proven by contradiction. Thus one assumes that there are two elements x and y in the universe U such that P(x) and P(y) are true and x != y. Then by a valid argument one arrives at the contradiction x = y—that is, x and y are the same element of U . Example: \
\
(∃ 0 ∈ Z)(∀m ∈ Z), m + 0 = m \
\
Proof: Assume, on the contrary, there exist two distinct additive identities 0, 0' ∈ Z which satisfy (1) m + 0 = m ∀m ∈ Z and (2) m + 0' = m ∀m ∈ Z.  Since equation (1) is true for every m ∈ Z, in (1) let m = 0', then (1) becomes (3) 0' + 0 = 0'. Since equation (2) is true for every m ∈ Z, in (2) let m = 0, then (2) becomes (4) 0 + 0' = 0. By Z3, the commutative theorem of addition for the integers, (5) 0' + 0 = 0 + 0'. Hence, from (3), (4), and (5) 0' = 0' + 0 = 0 + 0' = 0.
- **Side-Notes**: The Fundamental Theorem of Algebra includes polynomials with real coefficients too, since every real number is a complex number with its imaginary part equal to zero.
