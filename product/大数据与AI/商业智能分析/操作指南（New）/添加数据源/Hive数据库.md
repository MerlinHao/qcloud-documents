1. 在添加数据源首页单击 Hive 数据库，进入新建页面。
新建的页面如下：
 ![](https://main.qcloudimg.com/raw/cd2e0b6e54a7b041cc26b51ba0dfd56a.png)
 【选择数据源】默认是在首页选择的数据库类型。用户也可以在下拉列表里选择其它的数据库类型，此处选中的是 Hive。
【仅对有写权限的用户可见】如果 user1 对数据源只有读权限，对依赖此数据源的数据集有读或者读写权限，勾选此项，用 user1 登录，进入创建数据集模块，打开数据源会提示 “ 仅对有些权限的用户可见”，打开依赖此数据源的数据集，数据源信息是收起的且不可展开。
【驱动】用户可手动填写或选择需要的驱动类型。
【URL】设定数据源 URL。
【服务器登录】包含四种方式：用户名和密码、无身份验证、用户名、Kerberos。当数据库设定了访问权限后，用户需要使用用户名和密码或者只有用户名来访问当前数据库。

 选择 Kerberos 登录方式，界面展示如下：
 ![](https://main.qcloudimg.com/raw/9aaa97118466f490dfdfe53afd767700.png)
 【密钥文件路径】KeyTab 文件的路径，如： `/opt/xxx/user.keytab`
【Krb5 文件路径】Krb5 文件的路径。Linux 环境下 Krb5 文件的名字为   Krb5.conf；Windows 环境下名字为 Krb5.ini。Krb5 文件一般会放到一个默认的地方，这样就不需要去配置该项。如果客户不提供这个文件, 可能他们已经在默认位置放了。 一般来说，Windows 的默认位置是 `C:\Windows\Krb5.ini` 或者 `C:\winnt\Krb5.ini`；Linux的默认位置是` /etc/Krb5.conf `或者 `/etc/krb5/krb5.conf`。
【Jaas 文件路径】Jaas 文件的路径。该配置文件一般是用于 Zookeeper 安全认证的。 比如` /opt/xxx/jaas.conf`。
【用户名】用户所对应的 Kerberos Principal Name。
【最大连接数】该数据源最多的连接个数。
【队列名】Hadoop 设置任务执行的队列以及优先级。
【表结构模式】控制数据源下展示的表结构模式。当选择一个表结构模式，数据源下就只展示指定的这一个，如果此处不做指定，那将显示所有的表结构模式。
2. 填写相应的 Hive 数据库连接信息。
3. 单击测试连接，提示测试成功，即该数据源成功连接到相应数据库。
4. 单击菜单栏 > 保存，保存该数据源。创建数据集和制作报告模块都可以使用已保存的数据源。
