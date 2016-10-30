# city-query

```php
  	\$model=M('');
  	\$db_prefix=C('DB_PREFIX');
 	\$list=\$model
 	->field('o.*,r1.name as province_name,r2.name as city_name,r3.name as district_name,c.name as cate_name')
 	->table(\$db_prefix.'organ as o')
 	->join('LEFT JOIN '.\$db_prefix.'region AS r1 ON r1.id =o.province_id')
 	->join('LEFT JOIN '.\$db_prefix.'region AS r2 ON r2.id =o.city_id')
 	->join('LEFT JOIN '.\$db_prefix.'region AS r3 ON r3.id =o.district_id')
 	->join('LEFT JOIN '.\$db_prefix.'organcate AS c ON c.term_id =o.cate_id')
 	->where('o.audit=1')->select();
```

###### 功能:
三级城市的查询,查询机构对应的省市区和分类