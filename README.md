# Unexpected Values with Mutable Variables in F# Functions

This example demonstrates a common issue when working with mutable variables in F# functions.  The values passed to the function are copies; if the original variables are changed later, the function won't reflect those changes. This can lead to unexpected results when mutable variables are used without careful consideration of their scope and mutability.  The solution shows how to handle this correctly depending on the desired behavior. 

## Bug:
The `add` function uses the initial values of `x` and `y`, even though they are updated after the function call.  This is because the function operates on copies of the values passed to it, not on the original variables themselves. 