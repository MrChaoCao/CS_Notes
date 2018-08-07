# Redux and Thunk in React

## How we did it before Redux
component had to include logic to fetch data or itself
component had to have to be stored in a state

## Understanding redux
1. Global state, single source of truth
2. State can only be modified by emitting an action
  * action describes what should change in the state
  * action creators are the functions that dispatched to emit a change. They return an action.
3. Reducers actually change the state after taking in an emitted action.
4. Reducers are pure functions. They have no side-effects and do not mutate the state. They return a modified copy of the state.
5. Reducers are combined into a root reducer.
6. The store represents the state. It uses the rootReducer, and middleware and allows you to emit actions.
7. In React/Redux the Provider component wraps the whole application and passes the store down to all children.

## Designing the State
Action creators are different from actions. We have an action creator
