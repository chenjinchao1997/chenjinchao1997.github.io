# karma+Mocha+chai Vue Unit Test

nextTick 中的assert语句无法执行？

When using Vue.nextTick(*f()*), karma may skip the assert in the *f()*.
To solve this problem you should add `async` `await` to the `it()` function.

```javascript
it('OpinionInput.vue', async () => {
    ...
    await Vue.nextTick(() => {
        ...
    })
}
```

imitate click

```javascript
const clickEvent = new window.Event('click')
// 点击下拉框
const elselect = vm.$el.querySelector('.select')
elselect.dispatchEvent(clickEvent)
```
