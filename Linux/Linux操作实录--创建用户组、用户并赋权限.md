第一步：登录已有的Linux系统，使用root账户，登录好以后，如下图：

![214545_WlK5_2322439.png](http://static.oschina.net/uploads/space/2015/0304/214545_WlK5_2322439.png)

这样，就登录到Linux系统中，而且是用root用户登录的

注意：如果，你想要创建用户和用户组，那么你当前登录的用户必须有root权限，或者登录的就是root用户

第二步：创建组

![214839_R9Ts_2322439.png](http://static.oschina.net/uploads/space/2015/0304/214839_R9Ts_2322439.png)

如果，你不知道创建组的格式，那么就输入： groupadd --help,那么就会出现如上图出现的提示

注意：创建组的时候可以指定组的ID和组ID是否重复等，基本创建语句：groupadd 组名称

第三步：创建用户

![215221_kSlE_2322439.png](http://static.oschina.net/uploads/space/2015/0304/215221_kSlE_2322439.png)

同创建组一样，如果你不知道创建命令，就输入：useradd --help,就会出现提示

基本的创建语句：useradd -d /home/用户根目录 -m -g 用户组 用户名

上面语句中的-m是创建目录，-g 用户属于那个组

这样，我们就把用户组和用户都创建好了，那么下一步就是给新创建的用户修改密码

第四步：修改密码

![215708_LVz8_2322439.png](http://static.oschina.net/uploads/space/2015/0304/215708_LVz8_2322439.png)

修改用户的密码，根据提示输入两次密码，提示修改成功，这样，我们创建的用户就可以像正常用户一样登录了，但是到现在为止，我们创建的用户还不能像root一样去执行命令等，因为我们并没有给新建的用户赋权限，接下来，我们给用户赋权限

第五步：给用户赋权限

![220159_kgrn_2322439.png](http://static.oschina.net/uploads/space/2015/0304/220159_kgrn_2322439.png)

如上图所示，这是chown --help的提示信息，下面我们来写赋权语句

![220325_Esbw_2322439.png](http://static.oschina.net/uploads/space/2015/0304/220325_Esbw_2322439.png)

语句格式：chown -R 所有者:用户组  文件或者目录，-R是循环遍历的意思，把目录下的所有文件都归属给这个所有者。

第六步：修改文件夹权限

![220636_FnYd_2322439.png](http://static.oschina.net/uploads/space/2015/0304/220636_FnYd_2322439.png)

如果所示，上面是chmod --help的提示信息

语句格式： chmod -R 777 /home/需要修改权限的目录或者文件,-R是递归的意思，把这个目录下面的所有目录的权限都修改成为777

到此，登录root，创建用户组，创建用户、给用户指定目录，给目录指定权限就全部完成了，最后奉上文件夹所属组织和用户的截图

![222010_A9ct_2322439.png](http://static.oschina.net/uploads/space/2015/0304/222010_A9ct_2322439.png)