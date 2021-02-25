## 基础用法


```tsx
import { View, Text } from 'react-native';
import { Empty } from 'tant-rn';

const EmptyComponent = () => {
  return (
    <>
      <Empty
        mainDescription="主要描述"
        subDescription="次要描述"
        icon={{uri: 'https://xxxx', width: 100, height: 100}}
      >
        <View><Text>自定义</Text></View>
      </Empty>
    </>
  );
};

```

## API

### Props

| 参数 | 说明 | 类型 | 默认值 |
|------|------|------|------|
| mainDescription | 主要描述文案 | *string* | `''` |
| subDescription | 次要描述文案 | *string* | `''` |
| icon | 缺省图片 | EmptyImage | `default` |

#### EmptyImage

| 名称 | 说明 | 类型 |
|------|------|------|
| uri | 图片uri | *string* |
| width | 图片宽度 | *string \| number* |
| height | 图片高度 | *string \| number* ||