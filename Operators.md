### Like
	WHERE XXX LIKE '%AAA%' == WHERE XXX REGEXP 'AAA'
	在xxx列中检索含AAA的项

	'^field' - 以field开头 ==》 'field$' - 以field结尾
	
	'^field|ac|jsc' - 由｜分割，作为or；^仅跟随field
	'[gim]e' - ge or ie or me 
	'e[a-h]' - ea -> eh
	 

### IS NULL | IS NOT NULL
### DESC- decending降序

![[截屏2025-06-12 16.50.24.png]]
其中10 as point 意为 points列中所有值为10的项

## LIMIT clause
限制筛选数据个数

## INNER JOIN clause
	JOIN XXX ON AAA - 将xxx连接到aaa中

#三表插入：
![[截屏2025-06-12 17.29.49.png]]
![[截屏2025-06-12 17.30.07.png]]
JOIN XXX ON AAA = BBB
XXX为目标插入表
AAA为插入新表的列名，BBB为原表名
![[截屏2025-06-12 17.40.05.png]]
#### ON ... AND - compound joint condition

## OUTER JOIN
LEFT/RIGHT JOIN


```sql
USE sql_hr;
-- Database changed
```

