# Unexpected Behavior with Mutable Variables in F#

This repository demonstrates a common error in F# related to the use of mutable variables and pass-by-reference semantics.  The `swap` function attempts to swap two mutable variables, but due to the way mutation and references work in F#, the result is not what might be intuitively expected.

## Bug Description

The code intends to swap the values of two mutable variables, `x` and `y`. However, because mutable variables are passed by reference, the `swap` function modifies the original variables directly, leading to incorrect results.

## Solution

The solution demonstrates a way to correctly swap the values of the mutable variables, using a technique that avoids unexpected side effects.