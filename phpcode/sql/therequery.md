# there-query

```php
	\$comments_model=M('');
  	\$db_prefix=C('DB_PREFIX');
	\$user_comments=\$comments_model
	->field('u.*,d.service_name')
	->table(\$db_prefix.'user_comments as u')
	->join('LEFT JOIN '.\$db_prefix.'detection_service AS d ON d.service_id =u.service_id')
	->join('LEFT JOIN '.\$db_prefix.'organ AS o ON o.id=d.organ_id')
	->where("o.id={\$organ_id}")
	->select();
```


###### 功能:
三表左连接查询方法