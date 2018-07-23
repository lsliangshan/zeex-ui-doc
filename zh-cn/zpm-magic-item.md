# zpm-magic-item

> weex多功能item组件，可侧滑呼出更多操作按钮


### 使用方法

```vue
<template>
  <zpm-magic-item @delete="deleteItem" @click="add(index)">
    <div>
      <text>2018.07.07-至今</text>
      <text>项目名称</text>
    </div>
  </zpm-magic-item>
</template>

<script>
import ZpmMagicItem from 'path/to/ZpmMagicItem'
export default {
  components: { ZpmMagicItem },
  methods: {
    deleteItem () {
      console.log('delete item')
    },
    add (index) {
      console.log('add', index)
    }
  }
}
</script>
```

### 可配置参数

| Prop      | Type   |Required  | Default   | Description  |
|-------------|------------|--------|--------|-----|
| width | `Number` | `N`|  `750` | 宽度 |
| subItems | `Array` | `N`|  `[{text: '删除', event: 'delete'}]` | item的操作按钮，默认包含一个删除按钮，点击删除按钮会触发`delete`事件，触发的事件名可自定义 |

### Slot

1. `<slot></slot>`: 只有一个默认卡槽

### 事件回调

```
// 根据props中subItems字段，动态触发事件

// 固定回调事件 `@click="clickHandler"`

// subItems:
/**
  [
    {
      text: '删除',
      event: 'delete'
    },
    {
      text: '保存',
      event: 'save'
    }
  ]
  // 触发事件 `@delete="deleteHandler"`
  // 触发事件 `@save="saveHandler"`
 */

```
