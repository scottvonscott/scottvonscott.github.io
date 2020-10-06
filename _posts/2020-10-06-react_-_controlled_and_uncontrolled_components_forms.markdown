---
layout: post
title:      "React - Controlled and Uncontrolled Components/Forms"
date:       2020-10-06 22:54:33 +0000
permalink:  react_-_controlled_and_uncontrolled_components_forms
---


Coming off the heels of building frontends with Javascript and HTML, forms in React won’t feel all that dissimilar in how they are formatted. The key difference is how the data is handled, and as you may expect with React, it’s all going to depend on the value of state. When a component’s state dictates the form's input value, that’s called a Controlled Form.

Calling something “Controlled” implies a level of, well, control, and part of that distinction will require the flexibility of updating state, that way we’re not just stuck with a static value. Naturally we can use setState() to make the necessary updates and the best time to do so is immediately. Using the onChange event listener, we can ensure that all form inputs are reflected in our state right away.

```
<input type="text" onChange={event => this.handleEmailChange(event)} value={this.state.email} />
```

The form above would trigger the handle change function below:

```
handleEmailChange = event => {
  this.setState({
    email: event.target.value
  })
}
```

Once the state is updated, our components will rerender and with them the form value as well. Because we're connected to the state in this way, our form data is accessible wherever we've connected to that particular state. The next logical step you could do to your form is createg a onSubmit listener, which could take our form value and send if off elsewhere, like our back end server.

Although greater control over our applications is usually preferred (and recommended), customizing each form with multiple event listeners and their related functions can be a lot of work that you may or may not care to do. The easy (some might say "quick and dirty") alternative is an uncontrolled component, where the forms derive value directly from the DOM instead.

An uncontrolled component would retrieve a form element's value from the element's own internal state. Where we used the value property for a controlled form, we instead will use defaultValue property with uncontrolled (which is an easy way to quickly tell them apart too). We could set an initial value for the element with the defaultValue prop pretty easily.

```
<input
          defaultValue="myfullname@example.com"
          type="text"
          ref={this.input} />
```

Ref in the code above is what gives us access to the DOM nodes or a particular element.

If general consensus isn't enough to encourage mainly using controlled forms, another thing to consider is how controlled forms/components can help keep your data clean. When our handleChange function is triggered by the onChange event, we can actually validate the form data prior to setting state, and thus prevent the state, and by extension, the input from updating.

Controlled forms keep our form values bound to our component's state, meaning that the state remains our single source of truth. That familiar principle alone should encourage their use in applications, but uncontrolled components have their niche too.


