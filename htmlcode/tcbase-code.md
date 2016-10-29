### thinkcmf代码段

## 全局变量

thinkcmf封装了前台模板中一些常用的变量，可以在任何时候调用

```
{$site_name}			//站点名称            
{$site_host}                   //站点域名
{$site_root}  			//安装目录                
{$site_icp}    			//备案信息             
{$site_admin_email  	       //管理员邮箱      
{$site_tongji},               //页面统计代码     
{$site_seo_title}            //SEO标题
{$site_seo_keywords}         //SEO关键字
{$site_seo_description       //SEO描述
{$site_copyright}          //版权信息	

```

## 模板常量

```
__ROOT__   /网站根目录
__TMPL     /当前模板根目录
__PUBLIC__ /public 目录 不带/

```

## 常用代码段

- dtime

```
{$vo.createtime|date='Y-m-d',\#\#\#}

```
- tc_volist 

```
<volist name=\"$1\" id=\"$2\"></volist>
```

- tc_if

```
<if condition=\"$1\">\n$2$val\n<else />\n$3$val2\n</if>
```

