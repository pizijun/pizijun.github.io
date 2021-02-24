## 基础用法


```tsx
import { CountDown } from 'tant-rn';

const CountDownComponent = () => {

  const handleCountdownFinish = () => {
    console.log('finish');
  };

  return (
    <CountDown
      time={10000}
      onFinish={handleCountdownFinish}
    />
  );
};
```

## API

### Props

| 参数 | 说明 | 类型 | 默认值 |
|------|------|------|------|
| time | 倒计时时长 | *number \| string* | `0` |
| format | 时间格式 | *string* | `HH:mm:ss` |
| textStyle | 倒计时文字样式 | *React.CSSProperties \| any* | - |

### Events

| 事件名 | 说明 | 回调参数 |
|------|------|------|
| onFinish | 倒计时结束时触发 | - |