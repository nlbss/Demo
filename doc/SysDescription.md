# 定制化系统的修改说明

## 一.明确代码的位置

**1.  删除导航栏中的"编辑器"和"adminer"模块**

 实现：`\data\system\system_setting.php`删掉如下代码
 
    ,{"name":"editor","type":"system","url":"index.php?editor","target":"_self","use":"1"}
    ,{"name":"adminer","type":"","url":".\/lib\/plugins\/adminer\/","target":"_blank","use":"1"}

**2.  更改导航栏的标题**

实现：`\data\system\system_setting.php`中改为 "system_name":"AllView"

**3.  删除导航栏中的"文件管理"模块下方的路径**

实现：`\template\explorer\index.php`  47 行左右的 "id=yarnball" 的`<div>`

**4.  删除桌面图标(应用商店)**

实现：`\template\desktop\index.php` 33 行左右的  "class=file systemBox menuDefault" 的`<div>`

**5.  更改"文件管理"模块下方的商标**

实现：`\data\i18n\zh_CN\main.php`第   130 行和   131 行的 "copyright_info" 属性和 "copyright_pre" 属性

**6.  更改点击左下角图片后弹出的菜单**

实现：`\template\desktop\index.php` 删除  24 行左右  4 个`<li>`标签

**7.  删除"系统设置"模块中的"关于作品模块"**

实现：`\template\setting\index.php` 删除  29 行左右 "id=about" 的`<li>`标签

**8.  删除状态栏的显示桌面功能**

实现：`\template\desktop\index.php`的   45 行左右的 "class=taskbar_right" 的`<div>`

**9.  清空系统设置模块下的程序描述和新用户默认创建app**

实现：`\data\system\system_setting.php`

 删除 `\u2014\u2014\u8292\u679c\u4e91.\u8d44\u6e90\u7ba1\u7406\u5668`
 
 删除 `365\u65e5\u5386,pptv\u76f4\u64ad,ps,qq\u97f3\u4e50,\u641c\u72d0`
 
`\u5f71\u89c6,\u65f6\u949f,\u5929\u6c14,\u6c34\u679c\u5fcd\u8005,\u8ba1`

`\u7b97\u5668,\u8c46\u74e3\u7535\u53f0,\u97f3\u60a6\u53f0,icloud`   



## 二.通过捷径知道如何修改

**1.	更改左下角开始图标**

实现：`\static\images\desktop`的名为   "start.jpg" 图片，用一张图片来替换它
(图片尺寸：40 * 120)
          
**2.	删除其他桌面图标**

 实现：`\data\User\admin\home\desktop`不需要的图标给删掉(我剪切到了其上一级目录)

**3.    更换壁纸**

实现：`\static\images\wall_page`的名为   "7.jpg" 的图片，用一张图片来替换它

