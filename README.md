# timeout-transition-group

A React Transition Group better than CSSTransitionGroup.

This library is originally created by Khan Academy at [`timeout-transition-group`](https://github.com/Khan/react-components/blob/master/js/timeout-transition-group.jsx).
Many thanks to [Khan Academy](https://www.khanacademy.org)!

# Why TimeoutTransitionGroup instead of CSSTransitionGroup?

CSSTransitionGroup, provided as a React addon, is buggy.
Sometimes the animated component that is supposed to leave does not leave.

This is because CSSTransitionGroup component listens to CSS `transitionend` event which are not always sent.
TimeoutTransitionGroup fixes this bug by setting the timeout of animation.

# How to install

```
npm i --save timeout-transition-group
```

Use v2 or above for React 0.14, v1 for 0.13, and v0 for React 0.12.

# How to use

It's the quite similar to CSSTransitionGroup with two additional props, `enterTimeout` and `leaveTimeout`.
The values are in millisecond:

```
<TimeoutTransitionGroup
  enterTimeout={200}
  leaveTimeout={250}
  transitionName="transitionName">
  <div key="hello-world">Hello world!</div>
</TimeoutTransitionGroup>
```

# License

[MIT License](http://opensource.org/licenses/MIT)
