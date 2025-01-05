# Stale Closure in useEffect with setInterval
This example demonstrates a common error in React when using `setInterval` within the `useEffect` hook.  The closure created by `setInterval` captures the initial value of the state variable, leading to unexpected behavior.  The solution showcases how to correctly update state within `setInterval` using the functional update pattern.

## Bug
The `bug.js` file contains the erroneous code. The `setInterval` callback uses a stale closure that will always increment from the initial value of `count`, rather than the current value.