### upload-img

```php

     $upload = new \Think\Upload();// 实例化上传类
     $upload->maxSize   =     3145728 ;// 设置附件上传大小
     $upload->exts      =     array('jpg', 'gif', 'png', 'jpeg');
     // 设置附件上传类型
     $upload->rootPath  =     './'.C("UPLOADPATH"); // 设置附件上传根目录
     $upload->savePath  =     './organ/'; // 设置附件上传（子）目录
     $info   =   $upload->upload();

```

###### 功能:
传图片类操作