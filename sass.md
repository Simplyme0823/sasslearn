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
