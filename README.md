# vs2017ItemTemplates
vs2017模板

微软发布VS2017的时候，我第一时间离线一份专业版，安装到了自己的电脑上，开始体验，但是问题来了，在开发中建立类和接口的时候，说

明注释总要自己写一次，烦！~~于是还是像以前一样改IDE默认的类和接口的模板来实现，结果发现vs2017的和以前版本文件位置不一样，今天分享

出来我的修改，希望可以帮有同样需求的码友们

 

1、模板文件的路径。

C:\Program Files (x86)\Microsoft Visual Studio\2017\Professional\Common7\IDE\ItemTemplates\CSharp\Code\2052

几个文件夹看一眼就应该知道什么了吧，按自己的需要修改吧



2、注释的一些说明，还是和以前一样的。

参数                　　　　　　描述

clrversion            　　　　 当前系统CLR版本号

GUID [1-10]            　　　生成全局唯一标识符,可以生成10个 (例如:guid1)

itemname            　　　　 打开添加新建项时输入的文件名称

machinename            　　 当前机器的名称(如:pc1)

registeredorganization       注册的组织名

rootnamespace            　  命名空间名

safeitemname            　　 保存的文件名

time                　　　　　  当前系统时间,格式:DD/MM/YYYY 00:00:00.

userdomain            　　　 用户所在的域

username            　　　　 当前系统用户名

year                　　　　　  当前系统时间 YYYY

例如修改成下面：

/****************************************************************
 * 作    者：$userdomain$  $username$
 * CLR 版本：$clrversion$
 * 创建时间：$time$
 * 当前版本：1.0.0.1
 * 机器名称: $machinename$
 * 
 * 描述说明：$itemname$
 *
 * 修改历史：
 *
*****************************************************************
 * Copyright @ $username$ $year$ All rights reserved
*****************************************************************/
using System;
using System.Collections.Generic;
$if$ ($targetframeworkversion$ >= 3.5)using System.Linq;
$endif$using System.Text;
$if$ ($targetframeworkversion$ >= 4.5)using System.Threading.Tasks;
$endif$
namespace $rootnamespace$
{
    class $safeitemrootname$
    {
    }
}

效果会是这样的：


 /****************************************************************
 * 作    者：DESKTOP-QI3JKJT  yangw
 * CLR 版本：4.0.30319.42000
 * 创建时间：2018/9/5 16:23:27
 * 当前版本：1.0.0.1
 * 机器名称: DESKTOP-QI3JKJT
 * 
 * 描述说明：IConfigManager
 *
 * 修改历史：
 *
*****************************************************************
 * Copyright @ yangw 2018 All rights reserved
*****************************************************************/
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace rootnamespace
{
    class safeitemrootname
    {
    }
}