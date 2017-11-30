# cloudgo-data
golang 构建数据服务


# 任务要求：

使用 xorm 或 gorm 实现本文的程序，从编程效率、程序结构、服务性能等角度对比 database/sql 与 orm 实现的异同！ 

orm 是否就是实现了 dao 的自动化？

使用 ab 测试性能

参考 Java JdbcTemplate 的设计思想，设计 GoSqlTemplate 的原型, 使得 sql 操作对于爱写 sql 的程序猿操作数据库更容易。 
轻量级别的扩展，程序员的最爱

程序猿不怕写 sql ，怕的是线程安全处理和错误处理

sql 的 CRUD 操作 database/sql 具有强烈的模板特征，适当的回调可以让程序员自己编写 sql 语句和处理 RowMapping

建立在本文 SQLExecer 接口之上做包装，直观上是有利的选择

暂时不用考虑占位符等数据库移植问题，方便使用 mysql 或 sqlite3 就可以

参考资源：github.com/jmoiron/sqlx

# 基本要求
运行截图：

![curl_tem.png](http://upload-images.jianshu.io/upload_images/1039936-b4efc841057af0b5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)![userid_tem.png](http://upload-images.jianshu.io/upload_images/1039936-32c44bc45346c073.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![count.png](http://upload-images.jianshu.io/upload_images/1039936-07bd77caccc91684.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)![hello_id.png](http://upload-images.jianshu.io/upload_images/1039936-f4e57354a4a10f39.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



ab测试：

![tem_ab.png](http://upload-images.jianshu.io/upload_images/1039936-52949ac3c21fdc05.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![ab.png](http://upload-images.jianshu.io/upload_images/1039936-6f1db88bcf5c2613.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)









