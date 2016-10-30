# api-cerateWin

- 创建apicoud-win基本代码段

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="maximum-scale=1.0,minimum-scale=1.0,user-scalable=0,width=device-width,initial-scale=1.0"/>
    <title>win页面</title>
     <link rel="stylesheet" type="text/css" href="../../css/aui-win.css" />
    <style>
            
    </style>
</head>
<body>
   <header class="aui-bar aui-bar-nav" id="aui-header">
        <a class="aui-pull-left" tapmode onclick="api.closeWin()"> <span class="aui-iconfont aui-icon-left"></span> </a>
        <div class="aui-title">win页面</div>   
    </header>
    
    
</body>

<script type="text/javascript" src="../../script/api.js"></script>
<script type="text/javascript">
     apiready = function(){
        api.parseTapmode();
        var header = $api.byId('aui-header');
        $api.fixStatusBar(header);
        var headerPos = $api.offset(header);
        var body_h = $api.offset($api.dom('body')).h;
        api.openFrame({
            name: 'service_detail_frm',
            url: 'service_detail_frm.html',
            bounces: false,
           slidBackEnabled: 'false',
            rect: {
                x: 0,
                y: headerPos.h,
                w: 'auto',
                h: 'auto'
            }
        })

        
    };
</script>
</html>

```
## sublime代码段地址

[github地址][1]
  [1]: https://github.com/zhangwei699/mycode/blob/master/html/apicloud-template/api-cerateWin.sublime-snippet
