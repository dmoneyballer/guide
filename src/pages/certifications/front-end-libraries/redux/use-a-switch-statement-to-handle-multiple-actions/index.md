---
title: Use a Switch Statement to Handle Multiple Actions
---
## Use a Switch Statement to Handle Multiple Actions

Tip: Make sure you don't use "break" commands after return statements within the switch cases.

This is a stub. <a href='https://github.com/freecodecamp/guides/tree/master/src/pages/certifications/front-end-libraries/redux/use-a-switch-statement-to-handle-multiple-actions/index.md' target='_blank' rel='nofollow'>Help our community expand it</a>.

<a href='https://github.com/freecodecamp/guides/blob/master/README.md' target='_blank' rel='nofollow'>This quick style guide will help ensure your pull request gets accepted</a>.

<!-- The article goes here, in GitHub-flavored Markdown. Feel free to add YouTube videos, images, and CodePen/JSBin embeds  -->
A switch statement is another way to implement an if/else statement in JavaScript.  you start by declaring the switch with the expression you want to evaluate.
in this case, we want to evaluate the action.type so we would do that like this:

  switch (action.type) {
    
  }
 after we've done that we want to set our cases and the default. we set the cases by saying if the expression is equal to this value to the right of case, we want to execute this code. the default is if the expression doesn't match any of the case values.
  switch (action.type) {
    case 'LOGIN':return {authenticated: true}
    
    case 'LOGOUT':return {authenticated: false}

    default: return {authenticated: false}
  }
  
  The end code should look like this: 
  const defaultState = {
  authenticated: false
};

const authReducer = (state = defaultState, action) => {
  // change code below this line
  switch (action.type) {
    case 'LOGIN':return {authenticated: true}
    
    case 'LOGOUT':return {authenticated: false}

    default: return {authenticated: false}
  }
  // change code above this line
};

const store = Redux.createStore(authReducer);

const loginUser = () => {
  return {
    type: 'LOGIN'
  }
};

const logoutUser = () => {
  return {
    type: 'LOGOUT'
  }
};
