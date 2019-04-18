# Dialog
对话框组件。

## Usage

### 全部引入
```js
import { Dialog } from '@roo/roo-mobile-rn';
```

### 单独引入
```js
import Dialog from '@roo/roo-mobile-rn/dist/components/Dialog';
```

## Examples

![image](../images/Dialog/1.gif)

## Code
[详细 Code](../../examples/Dialog/index.tsx)

```jsx
import { Dialog } from '@roo/roo-mobile-rn';

<Dialog
  ref={(c) => {
    this._dialog = c
  }}
  cancelable={true}
  title='系统提示'
  bodyText='确认删除该信息？'
  cancelCallback={() => {
    console.log('cancel')
  }}
  confirmCallback={() => {
    console.log('confirm')
  }}
/>

this._dialog.open()
this._dialog.close()
```

## API

继承 [Modal](./Modal.md) 组件的所有 Props、Methods。

### Props

| Name | Type | Required | Default | Description |
| ---- | ---- | ---- | ---- | ---- |
| title | string | false | '标题' | 标题 |
| titleStyle | TextStyle | false | {} | 标题样式 |
| header | ReactElement | false | null | 自定义头部渲染区域 |
| bodyText | string | false | '内容' | 内容文本 |
| bodyTextStyle | TextStyle | false | {} | 内容文本样式 |
| body | ReactElement | false | null | 自定义内容渲染区域 |
| cancelLable | ReactElement | false | null | 自定义取消按钮渲染区域 |
| cancelLableText | string | false | '取消' | 取消按钮文本 |
| cancelLableTextStyle | TextStyle | false | {} | 取消按钮文本样式 |
| cancelCallback | Function | false | null | 取消按钮点击回调 |
| confirmLable | ReactElement | false | null | 自定义确认按钮渲染区域 |
| confirmLableText | string | false | '取消' | 确认按钮文本 |
| confirmLableTextStyle | TextStyle | false | {} | 确认按钮文本样式 |
| confirmCallback | Function | false | null | 确认按钮点击回调 |
| operationsLayout | string | false | 'row' | 操作按钮布局，支持 'row' 'column' |
| operations | Array | false | null | 自定义操作按钮组，该属性会覆盖前面的 cancel、confirm 按钮相关属性。数组元素为对象 { label: ReactElement, labelText: string, labelTextStyle: TextStyle, type: string, onPress: Function } |