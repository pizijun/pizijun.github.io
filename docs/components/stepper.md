## 基础用法


```tsx
import { Stepper } from 'tant-rn';

const StepperComponent = () => {

  const handleValueChange = (value: number) => {
    console.log(value);
  };

  return (
    <Stepper
      value="1"
      onChange={handleValueChange}
    />
  );
};
```

## API

### Props

| 参数 | 说明 | 类型 | 默认值 |
|------|------|------|------|
| value | 输入值 | *string* | `'0'` |

### Events

| 事件名 | 说明 | 回调参数 |
|------|------|------|
| onChange | 绑定的值发生变化时触发 | value:当前输入框的值 |