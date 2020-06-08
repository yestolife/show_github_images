# github中显示不出图片解决办法
参考文章：https://blog.csdn.net/qq_38232598/article/details/91346392
解决思路：显示不了github图片原因在于DNS污染，用本地host文件作为域名解析可绕过DNS污染。
解决办法：右击显示不出图片的地方，找到图片资源地址，在https://www.ipaddress.com/中查找域名对应的ip地址。将域名和地址对放入host文件中。Windows存放host文件的路径未：C:\Windows\System32\drivers\etc\hosts，在系统目录下，无法直接修改host文件，可通过拷贝出来，编辑后替换原文件。

20200608-host：
```
# GitHub Start 
140.82.113.3      github.com
140.82.114.20     gist.github.com

151.101.184.133    assets-cdn.github.com
151.101.184.133    raw.githubusercontent.com
151.101.184.133    gist.githubusercontent.com
151.101.184.133    cloud.githubusercontent.com
151.101.184.133    camo.githubusercontent.com
151.101.184.133    avatars0.githubusercontent.com
199.232.68.133     avatars0.githubusercontent.com
199.232.28.133     avatars1.githubusercontent.com
151.101.184.133    avatars1.githubusercontent.com
151.101.184.133    avatars2.githubusercontent.com
199.232.28.133     avatars2.githubusercontent.com
151.101.184.133    avatars3.githubusercontent.com
199.232.68.133     avatars3.githubusercontent.com
151.101.184.133    avatars4.githubusercontent.com
199.232.68.133     avatars4.githubusercontent.com
151.101.184.133    avatars5.githubusercontent.com
199.232.68.133     avatars5.githubusercontent.com
151.101.184.133    avatars6.githubusercontent.com
199.232.68.133     avatars6.githubusercontent.com
151.101.184.133    avatars7.githubusercontent.com
199.232.68.133     avatars7.githubusercontent.com
151.101.184.133    avatars8.githubusercontent.com
199.232.68.133     avatars8.githubusercontent.com

# GitHub End
```

