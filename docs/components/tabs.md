## 基础用法


```tsx
import React, { useState } from 'react';
import {  StyleSheet, View, Text } from 'react-native';
import { Tabs } from 'tant-rn';

const TabsComponent = () => {
  const tabs = [
    {title: 'tab 1'},
    {title: 'tab 2'},
    {title: 'tab 3'},
  ];

  const onTabChange = (tab: any, tabIndex: number) => {
    console.log(tab);
    console.log(tabIndex);
  };

  return (
    <>
      <Tabs
        tabs={tabs}
        page={1}
        tabBarInactiveTextColor="#BDB9C6"
        onChange={onTabChange}
      >
        <View><Text>tab 1</Text></View>
        <View><Text>tab 2</Text></View>
        <View><Text>tab 3</Text></View>
      </Tabs>
    </>
  );
};

```

## API

### Props

| 参数 | 说明 | 类型 | 默认值 |
|------|------|------|------|
| tabs | tab数据 | TabData | - |
| page | 当前 tab index | *sting \| number* | `0` |
| tabBarActiveTextColor | tab选中状态文字颜色 | *sting* | `'#5977FF'` |
| tabBarInactiveTextColor | tab非选中状态文字颜色 | *string* | `#333` |
| tabBarBackgroundColor | tabBar背景色 | *string* | - |
| tabBarTextStyle | tabBar文字样式 | *React.CSSProperties \| any* | - |
| tabBarUnderlineStyle | tabBar下划线样式 | *React.CSSProperties \| any* | - |

#### TabData

| 名称 | 说明 | 类型 | 必选 |
|------|------|------|------|
| title | tab标题 | *React.ReactNode* | true |
| key | tab key | *string* | false |

### Events

| 事件名 | 说明 | 回调参数 |
|------|------|------|
| onChange | 当前选中的tab改变时触发 | tab: TabData, index: number |
| onTabClick | 点击tab时触发 | tab: TabData, index: number |