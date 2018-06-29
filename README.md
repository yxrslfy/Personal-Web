# vue 中使用 font awesome


# 安装依赖

## 1. 安装基础依赖
```
$ npm i --save @fortawesome/fontawesome
$ npm i --save @fortawesome/vue-fontawesome
```

## 2. 安装样式依赖
```
$ npm i --save @fortawesome/fontawesome-free-solid
$ npm i --save @fortawesome/fontawesome-free-regular
$ npm i --save @fortawesome/fontawesome-free-brands
```

# 配置
进入main.js文件配置Font Awesome，配置方式比起4以前多了一些代码

```
import fontawesome from '@fortawesome/fontawesome'
import FontAwesomeIcon from '@fortawesome/vue-fontawesome'
import solid from '@fortawesome/fontawesome-free-solid'
import regular from '@fortawesome/fontawesome-free-regular'
import brands from '@fortawesome/fontawesome-free-brands'

fontawesome.library.add(solid)
fontawesome.library.add(regular)
fontawesome.library.add(brands)

Vue.component('font-awesome-icon', FontAwesomeIcon)
```

# 使用

原本 user 这个icon使用方法基本是 
```
<i class="fa fa-user"></i>
```

不过在Vue里不能这样直接使用了，要改为以下的写法：
```
<font-awesome-icon :icon="['fas','user']"/>
```
往icon属性里传入一个数组，第一个参数是样式，第二个就是图标名



特此以作记录
