# IO Reflection

## return multiple output in Javascript

Javascript doesn't natively support returning multiple values from function. It use a syntax called destructuring assignment to simulate this functionality. 
```javascript
function f1() {
  return [1, 2]
}
function f2() {
  return {
    c: 3,
    d: 4
  }
}
const [a, b] = f1()
const {c, d} = f2()
```
However, CGProto has not idea how to distinguish whether the returned value should be destructed, since array and object could be treated as single buffer, image or mesh. When you do need to return multiple values in you script, you can pack you values in a object with an additional field called destructuring that set to value of true.
![](_assets/4.png)
## limitation of shader reflection


- non-readOnly: