**1、环境确认： 将桌面缩放恢复成默认100% ，apt update 更新系统源信息。**
![image](https://github.com/xylogs/blog/assets/45510005/8bb9465c-6cd6-447c-a7f9-568ef9900ed6)

**2、以root权限安装GNOME:**
```
┌──(root㉿kali)-[~]
└─# tasksel
```

**3、选中GNOME并去掉Xfce。**

![image](https://github.com/xylogs/blog/assets/45510005/7d2b9dce-79f9-4622-a3ef-a111ed422396)

**4、设置默认桌面环境为gnome：**
```
┌──(root㉿kali)-[~]
└─# update-alternatives --config x-session-manager
There are 3 choices for the alternative x-session-manager (providing /usr/bin/x-session-manager).

  Selection    Path                    Priority   Status
------------------------------------------------------------
* 0            /usr/bin/xfce4-session   40        auto mode
  1            /usr/bin/gnome-session   50        manual mode
  2            /usr/bin/startxfce4      50        manual mode
  3            /usr/bin/xfce4-session   40        manual mode

Press <enter> to keep the current choice[*], or type selection number: 1
```

**5、重启系统使配置生效：**
```
┌──(root㉿kali)-[~]
└─# reboot
```

**6、重启后即可看到新桌面，命令查看结果：**
```
┌──(root㉿kali)-[~]
└─# update-alternatives --config x-session-manager
There are 3 choices for the alternative x-session-manager (providing /usr/bin/x-session-manager).

  Selection    Path                    Priority   Status
------------------------------------------------------------
  0            /usr/bin/gnome-session   50        auto mode
* 1            /usr/bin/gnome-session   50        manual mode
  2            /usr/bin/startxfce4      50        manual mode
  3            /usr/bin/xfce4-session   40        manual mode

Press <enter> to keep the current choice[*], or type selection number: 

```
