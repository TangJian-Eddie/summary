**Taro 全局变量**

utils 新建一个 global.js

```javascript
const globalData = {};
export const setGlobalData = (key, val) => {
  globalData[key] = val;
};
export const getGlobalData = (key) => {
  return globalData[key];
};
```

**Taro 自定义 navBar**

```html
<template>
  <view class="navBar">
    <view
      class="navigation-bar"
      :style="{'padding-top':`${paddingTop}px`,'height':`${height}px`,'line-height':`${height}px`,background:background,color:color,'font-size':fontSize}"
    >
      <view>{{ title }}</view>
    </view>
  </view>
</template>

<script>
  import Taro from "@tarojs/taro";
  export default {
    props: ["background", "color", "fontSize", "title"],
    data() {
      return {
        paddingTop: 44,
        height: 44,
      };
    },
    created() {
      //导航栏自适应
      let systemInfo = Taro.getSystemInfoSync();
      let reg = /ios/i;
      this.paddingTop = systemInfo.statusBarHeight; //导航状态栏上内边距
      const h = reg.test(systemInfo.system) ? 44 : 48;
      this.height = h;
    },
    method: {},
  };
</script>
<style>
  .navigation-bar {
    position: fixed;
    left: 0;
    top: 0;
    width: 750rpx;
    color: #000000;
    background: #ffffff;
    z-index: 99;
    text-align: center;
  }
</style>
```
