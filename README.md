# mpvue-star

> mpvue小程序评分

## 插件安装

## Build Setup

``` bash
npm i mpvue-star -D

```
## 使用
``` 
import MpvueStar from 'mpvue-star'
export default {
  components:{
      MpvueStar
    },
}

```
## 用法

```html
    <template>
  <div>
     <mpvue-star animate="animated bounceIn" color="#F05654">
         <template slot="icon"><i  class="i-star__text">❤</i></template>
    </mpvue-star>
  </div>
</template>
```

## 参数说明

| 参数        | 说明                      | 类型      | 可选值  | 默认值    |
| ---------  | ----------------------- | ------- | ---- | ------ |
| animate    | 动画效果     | String | -    | false   |
| color | 颜色 | String | - | - |

## 补充

- 使用过程中有任何问题，欢迎issue