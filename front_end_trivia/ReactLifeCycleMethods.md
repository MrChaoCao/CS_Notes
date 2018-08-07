# React Life Cycle Methods
## componentWillMount
+ component is not mounted yet
+ component is default posisiton
+ only useful for something that needs to happen before anything else, like an external API call
+ don't use it for AJAX calls

## componentDidMount
+ after component is there, this guarantees that your AJAX calls happen after the component is there to use it

## componentWillReceiveProps
+ called right before the component interacts with the new props
+ has access to current props and incoming props
+ if incoming props are different than current props, update. Note! Sometimes the props will not be different.

## shouldComponentUpdate
+ When componentWillReceiveProps is checking if the new props differ from the old props it calls on shouldComponentUpdate
+ Always returns a boolean value which checks to see if the props are the same.

## componentWillUpdate
+ Similar to componentWillReceiveProps but can't change the state
+ Used if you were using shouldComponentUpdate and needed to do something when props changed
+ Generally not very useful

## componentDidUpdate
+ Similar to componentDidMount. We can do the same things.
+ We use this because in componentWillReceiveProps the component might not have changed. Lets us avoid doing extra work on elements that have not updated.

## componentWillUnmount
+ Last call before component is removed
+ Cleanup for anything that involved this component.

## Resources:
[React Lifecycle Methods](https://engineering.musefind.com/react-lifecycle-methods-how-and-when-to-use-them-2111a1b692b1)
