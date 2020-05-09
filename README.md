# useBlur
复合表单组件控制blur事件

```shell script
npm i @kne/use-blur
```

# 使用说明

```jsx
import useBlur from '@kne/use-blur';

const SomeComponent = ()=>{
  const ref = useBlur(()=>{
    console.log('onBlur trigger');
  });
  return (
    <span ref={ref}>
      <input type="text"/>
      <input type="text"/>
    </span>
  );
};
```
上述示例组件中，SomeComponent组件中的任何一个元素触发focus然后点击组件外部区域都会触发onBlur，而在两个input之间来回focus不会触发onBlur

一般用于捕捉form的复合组件形成的field的校验时机