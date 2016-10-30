## php类常用操作

对应sublime代码段中的 路径 `Sublime 3\Data\Packages\mycode\php\php-base2.sublime-completions`

- cla

```php
//php控制器的基本创建
<?php
namespace Home\Controller;
use Common\Controller\AdminbaseController;
/**
 * ControllerName
 */
class NameController extends AdminbaseController{
	/**
	 * ActionName
	 */
	public function index(){
		
		$this->display();
	}

}
```

- mod

```php
模型的基本创建
<?php
namespace Common\Model;
use Common\Model\BaseModel;
/**
 * ModelName
 */
class NameModel extends BaseModel{
}
```
- model

```php
模型增删改查的基本创建
<?php
namespace Common\Model;
use Common\Model\BaseModel;
/**
 * ModelName
 */
class NameModel extends BaseModel{

	/**
	 * 添加数据
	 * @param	array	$data	数据 
	 * @return 	integer			新增数据的id 
	 */
	public function addData($data){
		$result=$this->add($data);
		return $result;
	}
	
	/**
	 * 修改数据
	 * @param	array	$map	where语句数组形式 
	 * @param	array	$data	数据 
	 * @return	boolean			操作是否成功
	 */
	public function editData($map,$data){
		$result=$this->where($map)->save($data);
		return $result;
	}
	
	/**
	 * 删除数据
	 * @param	array	$map	where语句数组形式
	 * @return	boolean			操作是否成功
	 */
	public function deleteData($map){
		$result=$this->where($map)->delete();
		return $result;
	}

	/**
	 * 传递主键id查找数据
	 * @param	integer	$id	主键id
	 * @return	array		查找到的数据
	 */
	public function getDataById($id){

		return $data;
	}

}
```

- php

```php

<?php  ?>
```
- status 

```php

判断性别取值
<php>=array('0'=>'待审核,'1'=>'已审核')</php> 
{$status[['status']]}
```

- dump

```php
dump($data);die;

```

- this

```php
$this
```
- m_val

```php
// 自动验证
protected $_validate=array(
    array('verify','require','验证码必填！'), //默认情况下用正则进行验证
    array('name','','帐号名称已经存在！',0,'unique',1), // 在新增的时候验证name字段是否唯一
    array('value',array(1,2,3),'值的范围不正确！',2,'in'), // 当值不为空的时候判断是否在一个范围内
    array('repassword','password','确认密码不正确',0,'confirm'), // 验证确认密码是否和密码一致
    array('password','checkPwd','密码格式不正确',0,'function'), // 自定义函数验证密码格式
);
```
- m_auto

```php
// 自动完成
protected $_auto=array(
    array('status',1),  // 新增的时候把status字段设置为1
    array('password','md5',1,'function') , // 对password字段在新增的时候使md5函数处理
    array('name','getName',1,'callback'), // 对name字段在新增的时候回调getName方法
    array('date','time',1,'function'), // 对date字段在新增的时候写入当前时间戳
);
```
- create

```php
// 对data数据进行验证
if(!$data=$this->create($data)){
    // 验证不通过返回错误
    return false;
}else{
    // 验证通过
    
}
```
- result

```php
if($result){
    // 操作成功
    $this->success('info',U(''));
}else{
    // 操作失败
    $this->error('name');
}
```
- ->add

```php
->add($data);
```
- full-url

```php
'http://'.$_SERVER['SERVER_NAME'].'/'.C('UPLOADPATH').$arr['thumb'];
```



