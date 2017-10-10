# html5-css3

### 记录一下 学习心得

## a 标签

a嵌套 文本内容的时候 一定要考虑设置成 block 或者inline-block; 
设置宽高 确定是否能被正常的覆盖要点击的区域 ;
不然就只能在文字上点击, 出了文字就不能正常的点击;

## a嵌套 图片的时候

a 无所谓是块元素还是内联元素; 都能被正常的点击到;


## img 标签

img 是内联元素, 它会默认产生一个内联框的 ,并且底部会有4像素的空白, (在被a标签包裹时候,这个4像素就可以看得到)
对其img 设置vertical-align: top 即可除去底部这空白误差;


## 比较常用的嵌套方式

div>a>img

div>a>文字

p>a>文字

ul>li>span>a>文字

ul>li>a>文字

form>div

div>div>div.....

a>span>文字

div>a 

ul>a>li>img+div+div (好处不需要设置a标签样式,可以对li 任意地方 进行点击跳转)

ul>li>a>img+div+div 

## 命名的技巧 (几乎都能命名)

基本的单词+位置

例如:名称     垂直排列                                           水平排列
top    top-hd top-bd top-ft                  top-rt top-mid top-lt;

header header-hd header-bd header-ft         header-rt header-mid header-lt;

nav    nav-hd nav-bd nav-ft                     nav-rt nav-mid nav-lt;

main   main-hd main-bd main-ft               main-rt main-mid main-lt;

menu   menu-service  menu-body   submenu box1 box2 box3

banner banner里面的img  num ...

##  一般交互的内容 并列分开写 

例如 :
nav>div.container  +  div.box1  +div.box2  ........

## 表示 在container里面的menu 点击对应的导航, 显示对应的box1 或box2 ...... 默认是都是display: none的