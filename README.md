# html5-css3

### 记录一下 学习心得

## a 标签

a嵌套 文本内容的时候 一定要考虑设置成 block 或者inline-block; 
设置宽高 确定是否能被正常的覆盖要点击的区域 ;
不然就只能在文字上点击, 出了文字就不能正常的点击;

a标签默认之间是有1em的空隙的,可以通过float解决

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

ul>a>li>img+div+div (好处不需要设置a标签样式,也可以对li 任意地方 进行点击跳转,  这是错误的写法, w3c不推荐,但是浏览器是可以解析出来的)  

ul>li>a>img+div+div 

## 命名的技巧 (几乎都能命名)

基本的单词+位置

例如:名称     垂直排列                                           水平排列

top    top-hd top-bd top-ft                  top-rt top-mid top-lt;

header header-hd header-bd header-ft         header-rt header-mid header-lt;

nav    nav-hd nav-bd nav-ft                     nav-rt nav-mid nav-lt;

main   main-hd main-bd main-ft               main-rt main-mid main-lt;

menu   menu-service  menu-body   submenu box1 box2 box3;

banner banner里面的img  num ...

hot  hot-title hot-content  

product

# 注: 一般a标签,p标签 都不需要加类名 ,导航做好用ul>li>a 进行嵌套 比较好遍历 也比较好 扩展


##  一般交互的内容 并列分开写 

例如 :
nav>div.container  +  div.box1  +div.box2  ........

## 而且container 最好不要把类名丢到一个div身上  不然 容易造成布局 混乱 ; 
## 表示 在container里面的menu 点击对应的导航, 显示对应的box1 或box2 ...... 默认是都是display: none的


# width 和 min-width 适用场景

width: 100%; 主要是使用在pc端页面

min-width: 1200px; 主要是 想要当pc端的页面能够较好的,全部呈现到移动端的时候,可以使用一下

min-width 是原来还没有media媒体查询的时代时候, 方案 ;

现在的移动端 主要是使用媒体查询和抛弃pc端,单独开发做法;

#注: 做移动端开发时候,要引入移动端的meta 标签设置,可以自动简单适配多种移动端

页面定期刷新，如果加url的，则会重新定向到指定的网页，content后面跟的是时间（单位秒），把这句话加到指定网页的<head></head>里
一般也用在实时性很强的应用中，需要定期刷新的
如新闻页面，论坛等，不过一般不会用这个，都用新的技术比如ajax等

<meta http-equiv="refresh" content="0; url=">'经过一段时间转到另外某个页面
content="0;URL="，这里0表示没有延时，直接跳转到后面的URL；把0改成1，则延时1秒后跳转。

网页自动计时跳转
这个页面跳转的好处在于不需要JS调用，直接在html文件头里加入 
<meta http-equiv="refresh[刷新-这里指定动作]" content="5[这里是时间];url=/article[这里是跳转的URL]"> 
当某个页面需要自动跳转的时候就要用到这个代码,比如一般的网站广告页面打开几秒后自动跳转到另外一个页面去就是用这个代码实现的(当然用js也是可以实现的)
  <!--[if lt IE 9]>
  
    <meta http-equiv="refresh" content="0;ie.html" />
    
  <![endif]-->