# wxdb
仿 YII1.1.5 QueryBuilder的数据库常用功能实现,用于在Swoole或者Workman等TCP高性能框架开发的时候使用.
#开发说明：
(1),必须安装PHP PDO扩展<br/>
(2),开发环境>=5.5<br/>
(3),如果不使用数据库连接池那么请使用DBConnection对象,如果要使用数据库连接池请使用DBPoolConnecion对象<br/>
(4),在使用数据库连接的时候必须先安装php-connection-pool扩展<br/>
(5),支持Composer<br/>
(6),使用实列<br/>
$dbConnection = new DBConnection($dns,$username,$password,null);<br/>
$users = $dbConnection->createCommand()<br/>
  ->select()<br/>
  ->from('user')<br/>
  ->where('id in' => array(1,2,3,4))->order('age desc')<br/>
  ->limit(2,5)<br/>
  ->queryAll();
#联系方式
mail.xiawei@163.com  如果有大牛发现bug，可以发送到我邮箱哦！！
