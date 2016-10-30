# tab-switch

```js
function fnOpenRelease(index_) {
		
		var status = $api.domAll("#tabbar li");
		// var tabbody = $api.byId('tabbody');
		// var content = $api.domAll(tabbody, '.collectList');	
		var content = $api.domAll('#tabbody .collectList');	
		// tab变样式
		for (var i = 0; i < status.length; i++) {
			$api.removeCls(status[i], 'active');
		}

		$api.addCls(status[index_], 'active');
		 // 列表改变
		for (var i = 0; i < content.length; i++) {
			$api.removeCls(content[i], 'show');
		}
		$api.addCls(content[index_], 'show');
	}
```

###### 功能:
tab切换特效
