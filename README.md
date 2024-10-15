# bluetooth
双系统蓝牙3.0适配
参考视频 https://www.bilibili.com/video/BV1PG4y1173i/?spm_id_from=333.337.search-card.all.click&vd_source=fcfa5e8f774bf0b67e92e038e70edd5f
参考文章 https://blog.csdn.net/weixin_43031092/article/details/120112317?spm=1001.2014.3001.5502

sudo apt install chntpw 安装修改注册表的软件chntpw
cd ~/Windows/Windows/System32/config
chntpw -e SYSTEM
cd ControlSet001\Services\BTHPORT\Parameters\Keys
ls cd file(only)
ls hex file
至此找到windows的linkkey
FA F1 9E 2A 1B 9F 29 21 6F 3D 6A AE EC 7C 26 61
在/var/lib/bluetooth找到linux配置的蓝牙设置 打开其中info文件修改其linkkey 
sudo systemctl restart bluetooth 重启蓝牙

ps--------------------------------------
https://zhuanlan.zhihu.com/p/693754050 clash使用

