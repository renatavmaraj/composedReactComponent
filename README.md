# Code can be used for any HOC

/*
Making use of higher order component

In some other location (not in this file)
We want to use this HOC

Example other file making use of this component

``
import Authentication //This is the HOC
import Resources // This is component I want to wrap

const ComposedComponent = Authentication(Resources)

in some render method...
<ComposedComponent />

``
So, you are not rendering the Resources, but the composition of 
the authentication and resources components

{...this.props} 

The expectation for receiving props is that you can access it when you call:
<Resources resourceList={resources} />

You will receive props via resourceList{resources}

Needs to make sure it ends up on target/child component

So when you return the composition of the Authentication HOC, together with
the resources component, 
