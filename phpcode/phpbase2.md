## php类常用操作

对应sublime代码段中的 路径 `Sublime 3\Data\Packages\mycode\php\php-base2.sublime-completions`

- cla

```
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

```
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

```
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

```
<?php  ?>
```
- status 

```

判断性别取值
<php>=array('0'=>'待审核,'1'=>'已审核')</php> 
{$status[['status']]}
```




