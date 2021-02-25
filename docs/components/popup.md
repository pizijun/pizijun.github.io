## 基础用法


```tsx
import React, { useState } from 'react';
import {  StyleSheet, TouchableHighlight, View, Text } from 'react-native';
import { Popup } from 'tant-rn';

const PopupComponent = () => {
  const [visible, setVisible] = useState(false);

  const onPress = () => {
    setVisible(true);
  };

  const handleClose = () => {
    setVisible(false);
  };

  return (
    <>
      <TouchableHighlight onPress={onPress}>
        <View style={styles.button}>
          <Text>点击</Text>
        </View>
      </TouchableHighlight>

      <Popup
        visible={visible}
        onClose={handleClose}
      >
        <View><Text>hello world</Text></View>
      </Popup>
    </>
  );
};

const styles = StyleSheet.create({
  button: {
    alignItems: "center",
    backgroundColor: "#DDDDDD",
    padding: 10
  },
});

```

## API

### Props

| 参数 | 说明 | 类型 | 默认值 |
|------|------|------|------|
| visible | 是否显示弹出层 | *boolean* | `false` |
| position | 弹出位置，可选top,bottom,center | *string* | `'center'` |
| customStyle | 自定义样式 | *React.CSSProperties \| any* | - |

### Events

| 事件名 | 说明 | 回调参数 |
|------|------|------|
| onClose | 关闭弹出层时触发	 | - |