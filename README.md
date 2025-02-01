# Expo Linking API Plus Symbol Decoding Bug

This repository demonstrates a bug in Expo's `Linking` API where plus symbols (+) in deep link query parameters are incorrectly decoded.  The bug causes unexpected behavior when handling deep links with parameters containing plus signs.

## Bug Description

When opening a deep link with a query parameter containing a plus symbol, the plus symbol is replaced with a space during the decoding process. This is not the expected behavior and can lead to issues in your app's logic.

## Reproduction Steps

1. Clone this repository.
2. Run the app in an Expo Go environment. 
3. Open the following deep link: `myapp://route?param=hello+world`
4. Observe the decoded value of the `param` parameter. It should be `hello world`, but it should be `hello+world`.

## Solution

A solution is provided in the `bugSolution.js` file.  This involves manually handling the decoding process to ensure that plus symbols are preserved.

## Note
This bug has been observed in Expo SDK 47 and might exist in other versions.
