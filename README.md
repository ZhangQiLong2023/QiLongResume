## 这是一份借鉴了许多优秀简历而制作出来的简历

>  [此简历借鉴于 Wu-SiLi 大佬的网页版本] 

## 确定主题色

> 在不使用 `node` 包的情况下，使用的 `vscode` 的 `Easy Less` 插件，将 `less`文件编译成 `css`文件。在 `less`文件中定义主题色变量 `$themeColor`，在使用主题色的地方使用变量替代。

```less
$themeColor: #0066FF;
.element{
  color:$themeColor;
}
```

## 确定网页尺寸

> 网页版简历和word版简历一样，都能打印成纸质版。A4纸张尺寸为21cm*29.7cm，那么网页与A4纸的比例相同即可。*
>
> *这里**网页宽度**我们选用为1024px**，那么**页面高度**=纸宽度/纸高度*网页宽度=29.7/21*1024=**1440px

```text
.page{
    width: 1024px;
    min-height: 1440px;
}
```

**代码块效果**

> 修改 `strong`默认样式，拥有 `代码块` 效果

```css
strong {
  font-family: 'Helvetica Neue', Helvetica, 'PingFang SC', 'Microsoft YaHei', '微软雅黑', Arial, sans-serif;
  font-size: 13px;
  line-height: 15px;
  font-weight: 500;
  color: #494949;
  margin: 0 3px;
  padding: 3px 8px;
  background-color: #F6F6F6;
  border-radius: 5px;
  border: 1px solid rgb(235, 235, 235);
}
```

> 使用时将代码块用 `<strong>` 标签包住即可

```html
熟悉<strong>HTML</strong>、<strong>JS(TS)</strong>、<strong>AJAX</strong>、<strong>ES6</strong>
```

### **修改滚动条**

```css
::-webkit-scrollbar {
  width: 5px;
  background-color: #f1f1f1;
}

::-webkit-scrollbar-thumb {
  background-color: rgba(0, 0, 0, 0.2);
  border-radius: 50px;
}

```

### **打印**

**A4尺寸为21cm\*29.7cm**

> 所以简历每页的大小比例相同即可

```css
.page{
    width: 1024px;
    min-height: 1440px;
}
```

**简历不只一页，不该断的地方在分页处了怎么办？**

<style>标签中添加media属性
> 值为 `print`，说明打印时才生效的样式  CSS `page-break-before ` 避免分页时内容的断开

```html
<style media="print">
    .page2{
        page-break-before:always;
    }
</style>
<section class=".page2">...</section>
```

**附上pdf简历下载链接**

> 在 `a` 标签上添加 `download` 属性就可以点击下载

```html
<a class="pdf" href="resume.pdf" download>
```

### **简历可编辑**

**怎么让别人拿你的简历改了就可以用?**

> 修改 `designMode` 属性

```js
document.designMode='on'
```

### **响应式**

> 适配不同宽度的效果

```css
@media screen and (max-width:1024px) {}
@media screen and (max-width: 720px) {}
```



