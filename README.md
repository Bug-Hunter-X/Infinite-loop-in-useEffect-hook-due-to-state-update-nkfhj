# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving an infinite loop caused by improperly using the `useEffect` hook.  The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version. 

**Bug:** The `useEffect` hook attempts to update the state (`count`) based on its current value within the dependency array.  This creates an infinite loop because each state update triggers a re-render, which then triggers the `useEffect` again.

**Solution:** The solution involves using the functional update pattern or removing the dependency. Removing the dependency should only be considered if the function does not rely on state change for its execution. Using the functional update pattern is better practice to avoid this problem.