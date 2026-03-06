# 下载自举备忘单 PDF 以供快速参考[更新]

> 原文：<https://hackr.io/blog/bootstrap-cheat-sheet>

flex-*-列

伸缩列以垂直显示内容(从上到下)。响应变量为 sm、md、lg、xl

```
<div class="d-flex flex-column"> <!--default size-->

<div class="d-flex flex-sm-column">...</div>
```

伸缩-*-列-反向

反转列的显示顺序

```
<div class="d-flex flex-column-reverse">
```

flex-*-row

一个接一个地水平显示内容(并排)。响应变量为 sm、md、lg、xl

```
<div class="d-flex flex-row">

<div class="d-flex flex-md-row">...</div>
```

柔性*-行-反向

反转行的显示顺序

```
<div class="d-flex flex-row-reverse">

<div class="d-flex flex-lg-row-reverse">...</div>
```

flex-*-nowrap

在 flex 容器中显示文本的默认设置

```
<div class="d-flex flex-nowrap">..</div>
```

弯曲*-缠绕

添加包装功能。响应变化——sm、ml、lg、xl

```
<div class="d-flex flex-wrap"> ... </div>

<div class="d-flex flex-xl-wrap"> ... </div>
```

弯曲*-缠绕-反向

逆序显示。

```
<div class="d-flex flex-wrap-reverse"> ... </div>

<div class="d-flex flex-xl-wrap-reverse"> ... </div>
```

flex-fill

用不同的颜色填充背景——主要颜色、次要颜色、信息颜色等

```
<div class="p-2 flex-fill bg-*">Flex item</div>
```

柔性*-增长-1

让指定的元素占据整个可用空间。

```
<div class="p-2 flex-grow-1 bg-primary">Flex grow</div>
```

弹性-*-增长-0

不要让项目在不同的屏幕上增长

```
<div class="p-2 flex-grow-0 bg-info">dont let me grow</div>
```

伸缩-1

让项目缩小

```
<div class="p-2 flex-shrink-1 bg-danger">Flex shrink</div>
```

伸缩-0

在不同的屏幕上没有缩小

```
<div class="p-2 flex-shrink-0 bg-primary">Flex no shrink</div>
```

对齐-内容-*-开始

更改项目的对齐方式(左对齐)

```
<div class="d-flex justify-content-start">

<div class="d-flex justify-content-sm-start">...</div>
```

对齐-内容-*-结束

证明到底(正确)

```
<div class="d-flex justify-content-end">

<div class="d-flex justify-content-sm-end">...</div>
```

对齐-内容-*-居中

居中对齐项目

```
<div class="d-flex justify-content-center">

<div class="d-flex justify-content-sm-center">...</div>
```

两端对齐-内容-*-之间

在项目之间对齐

```
<div class="d-flex justify-content-between">

<div class="d-flex justify-content-sm-between">...</div>
```

对齐-内容-*-左右

对齐项目周围的空间

```
<div class="d-flex justify-content-around">

<div class="d-flex justify-content-sm-around">...</div>
```

对齐-内容-*-开始

控制垂直对齐到起点(默认)

```
<div class="d-flex flex-wrap align-content-start">

<div class="d-flex align-content-sm-start">...</div>
```

对齐-内容-*-结束

将内容与结尾对齐

```
<div class="d-flex flex-wrap align-content-end">

<div class="d-flex align-content-sm-end">...</div>
```

对齐内容*居中

将内容居中对齐

```
<div class="d-flex flex-wrap align-content-center">

<div class="d-flex align-content-sm-center">...</div>
```

对齐-内容-*-周围

对齐项目周围的空间

```
<div class="d-flex flex-wrap align-content-around">

<div class="d-flex align-content-sm-around">...</div>
```

对齐内容*拉伸

拉伸单个伸缩盒项目

```
<div class="d-flex flex-wrap align-content-stretch">

<div class="d-flex align-content-sm-stretch">...</div>
```

对齐-项目-*-基线

相对于基线对齐项目

```
<div class="d-flex flex-wrap align-items-baseline">

<div class="d-flex align-items-sm-baseline">...</div>
```

对齐-项目-*-拉伸

将项目拉伸至柔性容器的全宽

```
<div class="d-flex align-items-stretch">

<div class="d-flex align-items-sm-stretch">...</div>
```

对齐自我*-开始

将单个弹性项目自对齐到起始位置(默认)

```
<div class="align-self-start">flex item align</div>

<div class="align-self-md-start">...</div>
```

对齐-自-*-结束

将单个 flex 项目自对齐到末端

```
<div class="align-self-end">flex item align</div>

<div class="align-self-md-end">...</div>
```

对齐自我*中心

将单个 flex 项目自动对齐到中心

```
<div class="align-self-center">flex item align</div>

<div class="align-self-md-center">...</div>
```

对齐自身*-基线

将单个弹性项目与基线自动对齐

```
<div class="align-self-baseline">flex item align</div>

<div class="align-self-md-baseline">...</div>
```

对齐-自身*-拉伸

拉伸至全宽

```
<div class="align-self-stretch">flex item align</div>

<div class="align-self-md-stretch">...</div>
```

订单-*-#

将特定弹性项目的显示顺序从 0-12 进行更改

```
<div class="order-12">first item</div> <!--will be displayed 12th-->

<div class="order-sm-3">ordered flex item</div>
```