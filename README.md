xyutils
---
[![npm](https://img.shields.io/npm/v/xyutils.svg)](https://www.npmjs.com/package/xyutils) 
[![Build Status](https://travis-ci.org/poetries/xyutils.svg?branch=master)](https://travis-ci.org/poetries/xyutils)
[![LICENSE MIT](https://img.shields.io/npm/l/xyutils.svg)](https://www.npmjs.com/package/xyutils) 

> 业务开发过程中，会经常用到`日期格式化`、`url参数转对象`、`浏览器类型判断`、`节流函数`等常用函数

usage
---

``` bash
$ npm install --save-dev xyutils
```

- 直接下载`min`目录下的[xyutils.min.js](https://github.com/poetries/xyutils/blob/master/min/xyutils.min.js)使用，支持`UMD`通用模块规范 

``` html
  <script src="xyutils.min.js"></script>
  <script>
      var OS = xyutils.getOS()
  </script>
```

> webpack、RequireJS、SeaJS等

``` javascript
// 完整引入
const xyutils = require('xyutils')
const OS = xyutils.getOS()
```

> 按需引入

``` javascript
// 只引入部分方法('xyutils/<方法名>')
const getOS = require('xyutils/getOS')
const OS = getOS()
```

``` javascript
// es6
const {getOS} from 'xyutils'
const OS = getOS()
```

API文档
---

**Array**

- `arrayEqual` 判断两个数组是否相等 
- `arrayContains` 检查数组中是否含有某元素 
- `arrayDescendeSort` 将数组进行递减排序 
- `arrayIncreaseSort` 将数组进行递增排序 

**Class**

- `addClass` 为元素添加`class ` 
- `hasClass` 判断元素是否有某个`class ` 
- `removeClass` 为元素移除`class`  

**Cookie**

- `getCookie` 根据`name`读取`Cookie`  
- `removeCookie` 根据`name`删除`Cookie`
- `setCookie` 添加`Cookie` 

**Device**

- `getExplore` 获取浏览器类型和版本号  
- `getOS` 获取操作系统类型
- `addFavorite` 加入收藏夹
- `getMobileScreenWidth` 获取移动设备屏幕宽度
- `isAndroidMobileDevice` 判断是否安卓移动设备访问
- `isAppleMobileDevice` 判断是否苹果移动设备访问
- `isMobile` 判断是否移动设备
- `isMobileUserAgent` 判断是否移动设备访问
- `setHomepage` 设为首页

**Dom**

- `getScrollTop` 获取滚动条距顶部的距离
- `offset` 获取一个元素的距离文档(`document`)的位置，类似`jQ`中的`offset()`
- `scrollTo` 在`${duration}`时间内，滚动条平滑滚动到`${to}`指定位置
- `setScrollTop` 设置滚动条距顶部的距离
- `windowResize` H5软键盘缩回、弹起回调

**Function**

- `debounce` 函数防抖   
- `throttle` 函数节流   

**Keycode**

- `getKeyName` 根据`keycode`获得键名 

**Object**  

- `deepClone` 深拷贝，支持常见类型
- `isEmptyObject` 判断`Object`是否为空

**Random**

- `randomColor` 随机生成颜色
- `randomNum` 生成指定范围随机数 

**Regexp**

- `isEmail` 判断是否为邮箱地址 
- `isIdCard` 判断是否为身份证号
- `isPhoneNum` 判断是否为手机号  
- `isTel` 验证是否为有效的座机电话号码  
- `isUrl` 判断是否为`URL`地址

**String**

- `digitUppercase` 现金额转大写

**Support**

- `isSupportWebP` 判断浏览器是否支持`webP`格式图片

**Time**  

- `formatPassTime` 格式化`${startTime}`距现在的已过时间
- `formatRemainTime` 格式化现在距`${endTime}`的剩余时间
- `isSameDay` 判断是否为同一天
- `getDate` 获取最近的日期
  - `getDate().DATE_TODAY`: 今天
  - `getDate().DATE_YESTERDAY`: 昨天
  - `getDate().DATE_1_WEEK_BEFORE`: 最近一周
  - `getDate().DATE_2_WEEKS_BEFORE`: 最近两周
  - `getDate().DATE_3_WEEKS_BEFORE`: 最近三周
  - `getDate().DATE_1_MONTH_BEFORE`: 最近一个月
  - `getDate().DATE_2_MONTH_BEFORE`: 最近两个月
  - `getDate().DATE_3_MONTHS_BEFORE`: 最近三个月
  - `getDate().DATE_1_YEAR_BEFORE`: 一年前
  - `getDate().DATE_3_MONTHS_AFTER`: 未来三个月
  - `getDate().DATE_1_YEAR_AFTER`: 未来一年
  - `getDate().DATE_FIRST_DAY_OF_MONTH`: 元旦
  - `getDate().DATE_LAST_DAY_OF_MONTH`: 本月的最后一天

**Url**

- `parseQueryString` `url`参数转对象
- `stringfyQueryString` 对象序列化
- `removeUrlPrefix` 去掉url前缀
