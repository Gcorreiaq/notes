# Scope
- [Redux-thunk](#redux-thunk)
- [Algorithms](#algorithms)

# Redux-thunk

- **Thunk action creators**: the functions that receive their arguments and contain an async function receiving ```dispatch``` and ```getState```.
```
export function fetchTodoById(todoId)
{
    // fetchTodoById is the thunk function
    return async function fetchTodosThunk(dispatch, getState)
    {
        const response = await client.get(`/fakeapi/todo/${todoid}`)
        dispatch(todosLoaded(response.todos))
    }
}
```

# Algorithms

- **Recurrences**: Functions frequently used in formal analysis of recursive algorithms.
- **Polynomial-Time algorithm**: Algorithms whose complexity is less than or equal to O(n^k), where k is a constant.
- **Side-Notes**: A good question: _Suppose we have two algorithms to solve the same problem. One runs in time T1(n) = 400n, whereas the other runs in time T2(n) = n2. What are the complexities of these two algorithms? For what values of n might we consider using the algorithm with the higher complexity?_ \
\
A: The complexity of T1 is O(n), and the complexity of T2 is O(n2). However, the algorithm described by T1 involves such a large constant coefficient for n that when n < 400, the algorithm described by T2 would be preferable. This is a good example of why we sometimes consider other factors besides the complexity of an algorithm alone.

