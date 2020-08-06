<!-- @format -->

\$为变量符号

在变量后面加上!default 即为默认变量，如果要覆盖默认变量 就在默认变量前面再次声明一下变量就可以了

```scss
$baseLineHeight: 2;
$baseLineHeight: 1.5 !default;

body {
  line-height: $baseLineHeight;
}
```

!global

### 混合宏 @mixin name -> @include name

相同代码块在不同的环境传递不同的值，可以通过宏来复用代码块
一般需要【传递变量】的时候都建议使用宏
缺点：不能合并相同的代码块，造成代码冗余

### 继承 @extend

相同代码块不需要传递不同的值，并且已经在 sass 文件中定义了，可以使用继承来调用基类将相同的基类代码合并
缺点：如果基类并不存在于 HTML 结构中，不管调用不调用，编译后的 CSS 都有基类的代码，造成了冗余

### 占位符 %placeholder -> @extend placehloder

克服了继承的缺点，当用占位符表示基类的时候，如果占位符基类没有被调用，那么编译后的 CSS 文件是不会有基类 CSS 样式的，并且如果多次调用了相同的基类，会进行代码合并

### 注释

在 scss 文件中 /\*\*/ 会被编译在 css 文件中 而//则不会

### 数据类型

数字：1,2,10px
字符串："foo",bar
颜色：blue,#ffffff, rgba(0,0,0,1)
布尔型：true,false
空着：null
值列表：空格/逗号分开 1.5em 1em 0 2em, Helvetica, Arial, sans-serif
