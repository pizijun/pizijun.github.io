## 基础用法


```tsx
import React, { useEffect, useRef, useState } from 'react';
import {  StyleSheet, TouchableHighlight, View, Text } from 'react-native';
import { Overlay } from 'tant-rn';

const OverlayComponent = () => {
  const [visible, setVisible] = useState(false);

  const onPress = () => {
    setVisible(true);
  };

  const handlePressOverlay = () => {
    setVisible(false);
  };

  return (
    <>
      <TouchableHighlight onPress={onPress}>
        <View style={styles.button}>
          <Text>点击</Text>
        </View>
      </TouchableHighlight>

      <Overlay visible={visible} onBackdropPress={handlePressOverlay}>
        <View><Text>hello world</Text></View>
      </Overlay>
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
| visible | 是否显示遮罩层 | *boolean* | `false` |
| lock | 是否锁定遮罩层，为true的话点击遮罩层不会隐藏 | *boolean* | `false` |
| backdropStyle | 自定遮罩层样式 | *React.CSSProperties \| any* | - |

### Events

| 事件名 | 说明 | 回调参数 |
|------|------|------|
| onBackdropPress | 点击遮罩层时触发 | - |