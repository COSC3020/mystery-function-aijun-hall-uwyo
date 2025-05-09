# Mystery Function

What does the `mystery()` function in the following piece of code do? Add your
answer to this markdown file.

```javascript
function mystery(a) {
    if(a.length == 1) return a[0];
    var foo = mystery(a.slice(1, a.length))
    if(foo > a[0]) return foo;
    else return a[0];
}
```

The `mystery()` function returns the maximum value in the input array `a` by using recursion to compare elements.

The base case for this function is if the array only has one element, then it returns that one element. (first if conditional)

The recursive case calls `mystery()` on the array excluding the first element `a.slice(1)`, and then compares
that result with the first element `a[0]`. (second if conditional)

If that value (which is stored in `foo`) is larger than `a[0]`, then it returns that value.

Otherwise it returns `a[0]`.

"I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice."