## 基础用法


```tsx
const NavbarComponent = () => {
  return (
    <NavBar
      title="页面标题"
      rightText="按钮"
    />
  );
};
```

## API

### Props

| 参数 | 说明 | 类型 | 默认值 |
|------|------|------|------|
| title | 标题 | *string* | `''` |
| rightText | 右侧文案 | *string* | `''` |
| rightIcon | 右侧Icon | RightIcon | - |


#### RightIcon

| 名称 | 说明 | 类型 |
|------|------|------|
| uri | 图片uri | *string* |
| width | 图片宽度 | *string \| number* |
| height | 图片高度 | *string \| number* |

### Events

| 事件名 | 说明 | 回调参数 |
|------|------|------|
| onPressRight | 点击右侧按钮时触发 | - |
| onPressBack | 点击左侧返回按钮时触发，当监听了此事件，页面返回需要自行处理 | - |