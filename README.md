### 引入组件

```
// index.wpy
<template>
    <heiToast></heiToast>
</template>
<script>
    import wepy from 'wepy';
    import heiToast from 'heiToast';

    export default class Index extends wepy.page {
        components = {
            heiToast
        };
    }
</script>
```

### 调用方法

```
let promise = this.$invoke('heiToast', 'show', {
    title: '自定义标题',
    icon: 'http://b347.photo.store.qq.com/psb?/V110hUaC2ecM8F/dP1DeJMTCUD25g*cX01K6zMs.wJgdjIhIX*C7sBkEUI!/m/dFsBAAAAAAAAnull&bo=1gC*AAAAAAARB1k!&rf=photolist&t=5',
});

promise.then((d) => {
    console.log('toast done');
});
```