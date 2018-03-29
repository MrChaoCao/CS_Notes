# React Life Cycle Methods
## componentWillMount
+ component is not mounted yet
+ component is default posisiton
+ only useful for something that needs to happen before anything else, like an external API call
+ don't use it for AJAX calls

## componentDidMount
+ after component is there, this guarantees that your AJAX calls happen after the component is there to use it
+

## componentWillReceiveProps
