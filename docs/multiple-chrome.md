
# 谷歌chrome多个相同用户登陆同一个机器多开配置
chrome的版本升到49之后，跨域设置比以前严格了，在打开命令上加--disable-web-security之后还需要给出新的用户个人信息的目录。众所周知chrome是需要用gmail地址登录的浏览器，登录后就会生成一个存储个人信息的目录，保存用户的收藏、历史记录等个人信息。49版本之后，如果设置chrome浏览器为支持跨域模式，需要指定出一个个人信息目录，而不能使用默认的目录，估计是chrome浏览器怕用户勿使用跨域模式泄露自己的个人信息（主要是cookie，很多网站的登录token信息都是保存在cookie里）。

- 关闭所有谷歌浏览器的页面

- 右键点击谷歌图标，找到属性 -> 快捷方式 -> 目标 

- 在后面加上这句话  --disable-web-security --user-data-dir=%LOCALAPPDATA%\Google\Chrome\%SessionName%

注意：要有空格！！！

- 应用后再次打开谷歌浏览器，OK！


