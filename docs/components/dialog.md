## 基础用法


```tsx
import React, { useEffect, useRef, useState } from 'react';
import {  StyleSheet, TouchableHighlight, View, Text } from 'react-native';
import { Dialog } from 'tant-rn';

const DiaglogComponent = () => {
  const [visible, setVisible] = useState(false);

  const onPress = () => {
    setVisible(true);
  };

  const handleCancel = () => {
    console.log('you clicked cancel button');
    setVisible(false);
  };

  const handleConfirm = () => {
    console.log('you clicked confirm button');
    setVisible(false);
  };

  return (
    <>
      <TouchableHighlight onPress={onPress}>
        <View style={styles.button}>
          <Text>点击</Text>
        </View>
      </TouchableHighlight>

      <Dialog
        visible={visible}
        title="提示"
        message="这是弹框"
        onCancel={handleCancel}
        onConfirm={handleConfirm}
      />
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
| visible | 是否显示弹框 | *boolean* | `false` |
| title | 标题 | *string* | `''` |
| message | 文本内容 | *sting \| React.ReactNode* | `''` |
| messageAlign | 文本内容对齐格式：left,center,right | *string* | `left` |
| confirmButtonText | 确认按钮的文案 | *string* | `确认` |
| cancelButtonText | 取消按钮的文案 | *string* | `取消` |
| showConfirmButton | 是否显示确认按钮 | *boolean* | `true` |
| showCancelButton | 是否显示取消按钮 | *boolean* | `true` |
| type | 弹框类型：alert,prompt | *string* | `alert` |
| placeholder | 输入框placeholder，只有当 type 为 prompt 有效 | *string* | `''` |
| inputValue | 输入框的默认值，只有当 type 为 prompt 有效 | *string* | `''` |

### Events

| 事件名 | 说明 | 回调参数 |
|------|------|------|
| onCancel | 点击确认按钮时触发	 | - |
| onConfirm | 点击取消按钮时触发	 | - |