# <center>导航栏制作（实践flex布局和scss）5.19</center>

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
  <link rel="stylesheet" type="text/css" href="http://at.alicdn.com/t/font_3410033_85ns0y7zkkk.css">
  <script src="https://cdn.staticfile.org/jquery/1.10.2/jquery.min.js"></script>
  <script>
    $(function(){

      $("#theFirst").click(function(){
        $(this).parent().children("a:lt(5)").slideToggle("fast");
      });

      $("#theSecond").click(function(){
        $(this).parent().children("a:gt(4)").slideToggle("fast");
      });

      $("a").click(function(){
        $("a").not(this).css('background','#263238');
        $("a").not(this).css('color','white');
        $(this).css('background-color','black');
        $(this).css('color','wheat');
      });

      $("a1").hover(function(){
        $(this).css("color","#F7BD00");
      },function(){
        $(this).css("color","white");
      });

      $("a").hover(function(){
        $(this).css("color","#F7BD00");
      },function(){
        if($(this).css("background-color")=="rgb(0, 0, 0)"){
          $(this).css("color","wheat");
        }
        else{
          $(this).css("color","white");
        }
      });
    });
  </script>
</head>

<body>
  <div class="topbar">
    <p>左边菜单栏暂时连接一些常见网站</p>
  </div>

  <div class="sorce">
    <div class="navigation">
      <a1 id="theFirst">监控中心</a1>
      <a href="https://www.bilibili.com/" class="daohang" target="d"><i class="iconfont icon-shishishuju"></i>实时数据</a>
      <a href="http://www.kugou.com/" class="daohang" target="d"><i class="iconfont icon-guanzhu1"></i>关注</a>
      <a href="https://y.qq.com/?ADTAG=myqq#type=index" class="daohang" target="d"><i class="iconfont icon-lishishuju"></i>历史数据</a>
      <a href="https://music.migu.cn/v3" class="daohang" target="d"><i class="iconfont icon-shijian"></i>事件数据</a>
      <a href="https://www.youku.com/" class="daohang" target="d"><i class="iconfont icon-shebeishuju"></i>未安装事件数据</a>
      <a1 id="theSecond">系统管理</a1>
      <a href="https://v.qq.com/" class="daohang" target="d"><i class="iconfont icon-jizhuangxiang"></i>集装箱管理</a>
      <a href="https://www.iqiyi.com/" class="daohang" target="d"><i class="iconfont icon-bumen"></i>部门管理</a>
      <a href="https://github.com/" class="daohang" target="d"><i class="iconfont icon-jiaosequnti"></i>角色管理</a>
      <a href="https://www.acfun.cn/" class="daohang" target="d"><i class="iconfont icon-shebei"></i>设备管理</a>
      <a href="https://leetcode-cn.com/" class="daohang" target="d"><i class="iconfont icon-user"></i>账号管理</a>
    </div>

    <iframe name="d" class="neiron" frameborder="0"></iframe>
  </div>
</body>

</html>
```

### 运行展示

![运行展示](./41.png "运行展示")

![运行展示](./42.png "运行展示")
