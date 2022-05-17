# <center>导航栏制作（实践flex布局和scss）5.17</center>

### scss设计：
```scss
body{
    background-color: rgb(214, 232, 239);
    display: flex;
    flex-direction:column;
    height: auto;
   
}
.topbar {
    height: 50px; 
    width: 100%;
    background-color: rgb(214, 232, 239);
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    p{
        line-height: 15px;
        margin: auto;
        font-size: 30px;
        color: rgb(18, 18, 17);;
     }

}

.sorce {
    height: auto;
    width: 100%;
    background-color: rgb(250, 239, 239);
    display: flex;
    justify-content: flex-start;
    .navigation  {
        height: auto;
        width: 250px ;
        background-color: #263238;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        a{
            text-decoration: none;
            text-indent: 20px;
            height: 200px;
            counter-reset: section;
        }
        a:hover{
            color: #F7BD00;
        }
        a1{
            text-indent: 20px;
            font-weight:bolder;
            text-decoration: none;
            color: #FFFFFF;
            text-align: left;
            line-height: 50px; 
            margin-top: 0px;
            flex: 0;
            display: flex;
            align-items: center;
            justify-content: left;
        }
        :nth-child(2)::before{
            content:url(./iconfont/con1.png);   
            display: flex;
            align-items: center;
        }
        :nth-child(3)::before{
            content:url(./iconfont/con2.png);
            display: flex;
            align-items: center;
        }
        :nth-child(4)::before{
            content:url(./iconfont/con3.png);
            display: flex;
            align-items: center;
        }
        :nth-child(5)::before{
            content:url(./iconfont/con4.png);
            display: flex;
            align-items: center;
        }
        :nth-child(6)::before{
            content:url(./iconfont/con5.png);
            display: flex;
            align-items: center;
        }
        :nth-child(8)::before{
            content:url(./iconfont/con6.png);
            display: flex;
            align-items: center;
        }
        :nth-child(9)::before{
            content:url(./iconfont/con7.png);
            display: flex;
            align-items: center;
        }
        :nth-child(10)::before{
            content:url(./iconfont/con8.png);
            display: flex;
            align-items: center;
        }
        :nth-child(11)::before{
            content:url(./iconfont/con9.png);
            display: flex;
            align-items: center;
        }
        :nth-child(12)::before{
            content:url(./iconfont/con10.png);
            display: flex;
            align-items: center;
        }
    }
    .neiron {
        width: 100%;
        height: 900px;
    
    }
    .daohang{
        background-color: #263238;
        line-height: 50px; 
        margin-top: 0px;
        text-align: left;
        color: #FFFFFF;
        flex: 0;
        display: flex;
        align-items: center;
        justify-content: left;
        flex-shrink: 0;
        img{
            display: flex;
        }
    }
}
```
### html

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Document</title>
  <link rel="stylesheet" type="text/css" href="./menu.css" />
</head>

<body>

  <div class="topbar">
    <p>左边菜单栏暂时连接一些常见网站</p>
  </div>

  <div class="sorce">
    <div class="navigation">
      <a1>监控中心</a1>
      <a href="https://www.bilibili.com/" class="daohang" target="d" onclick="changeColor(this)">实时数据</a>
      <a href="http://www.kugou.com/" class="daohang" target="d" onclick="changeColor(this)">关注</a>
      <a href="https://y.qq.com/?ADTAG=myqq#type=index" class="daohang" target="d" onclick="changeColor(this)">历史数据</a>
      <a href="https://music.migu.cn/v3" class="daohang" target="d" onclick="changeColor(this)">事件数据</a>
      <a href="https://www.youku.com/" class="daohang" target="d" onclick="changeColor(this)">未安装事件数据</a>
      <a1>系统管理</a1>
      <a href="https://v.qq.com/" class="daohang" target="d" onclick="changeColor(this)">集装箱管理</a>
      <a href="https://www.iqiyi.com/" class="daohang" target="d" onclick="changeColor(this)">部门管理</a>
      <a href="https://github.com/" class="daohang" target="d" onclick="changeColor(this)">角色管理</a>
      <a href="https://www.acfun.cn/" class="daohang" target="d" onclick="changeColor(this)">设备管理</a>
      <a href="https://leetcode-cn.com/" class="daohang" target="d" onclick="changeColor(this)">账号管理</a>
    </div>

    <iframe name="d" class="neiron" frameborder="0"></iframe>
    <script type="text/javascript">
      function changeColor(obj) {
        allObj = document.getElementsByClassName("daohang");
        for (var i = 0; i < allObj.length; i++) {
          allObj[i].style.background = 'rgb(15, 10, 90)';
          allObj[i].style.color = 'wheat';
        }
        obj.style.background = 'black';
        obj.style.color = 'white';
      }	
    </script>
  </div>
</body>

</html>
```

### 运行展示

![运行展示](./2.png "运行展示")
