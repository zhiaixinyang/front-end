> 工欲善其事必先利其器，Chrome浏览器应该算是前端开发人员最常用的工具了，本期带来一些很实用的chrome浏览器调试方法

## 用好Chrome Devtools
### console的骚操作
* congsole.log()、console.error()、console.warn()、console.info(): 常规打印数据信息
* console.table(): 表格形式打印复杂的数据结构
* console.group()、console.groupEnd(): 分组打印信息
* console.assert(): 条件打印
* console.dir(): 递归打印对象的所有属性
* console.trace(): 追踪函数的调用轨迹
* 带样式打印
![带样式打印](../images/console.jpg)

### 检查无用的css/js
* more tools=>Coverage
![检查没用的CSS/JS](../images/coverage.jpg)

### 断点检查
* hover、active

### 模拟断网进行错误处理
* offline

### 用timeline/performance查看执行时间
* 格子代表帧率
* 黄色js CPU占有率
* 红色 失帧比较厉害
* 紫色css CPU占有率

### 检查内存泄漏
* Memory=>profiles

### 查看内存消耗
* Memory=>profiles=>ALLOCATION TIMELINES

## 浏览器并发请求数量问题
* 基于端口数量和线程切换开销的考虑,浏览器不可能无限量的并发请求
* 并非越大越好，基于良知和默契的考虑，保护浏览器和服务器更好的性能
* 迅雷、暴风影音等可以修改电脑的最大连接数
* 用户可以重写浏览器的默认值(IE)
* 目前浏览器的最大同域并发请求数量
	
Browser|Max
:--:|:--:
IE8,9| 6
Firefox|6
Chrome|6

* [已有解决方案](https://www.zhihu.com/question/20474326/answer/15696641)：domain hash, cookie free, css sprites, js/css combine, max expires time, loading images on demand