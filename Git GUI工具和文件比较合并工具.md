# Git GUI工具和文件比较合并工具

**Git GUI Tools and File Diff and Merge Tools**

常用版本控制工具

* P4V Client - 企业工具，功能强大，付费
* Github Desktop - 免费工具，功能较少
* SourceTree - 免费工具
* Tower - 付费
* GitKraken - 付费，功能强大

常用文件比较合并工具

* Beyond Compare 4 - 功能强大，付费，试用30天
* DiffMerge - 免费，功能齐全
* FileMerge - XCode自带比较工具，操作简单
* Ultra Compare - 付费，功能强大，可以比较二进制、十六进制文件等等



### SourceTree

#### SourceTree下载和配置

LINK：https://www.sourcetreeapp.com/

下面介绍MacOS中相关配置

1. 绑定用户：菜单栏SourceTree - Preference - Accounts 可以进行用户绑定
2. 菜单栏SourceTree - Preference - General 推荐讲语言设置为English，否则可能试用不了Advanced选项，在Advanced选项中可以修改不同URL对应用户名
3. 在主菜单中点击New按钮，可以通过URL方式添加远程仓库



#### 为SourceTree配置文件比较合并工具

* Beyond Compare 4

  * 下载地址：https://www.scootersoftware.com/download.php

  * 安装后：菜单栏 - Beyond Compare - 安装命令行工具

  * 在SourceTree中：菜单栏 - Sourcetree - Preferences - Diff

    * 在Visual Diff Tool中选择Beyond Compare，在Merge Tool中选择Beyond Compare
    * 如果上述方法无法奏效，则在Visual Diff Tool中选择Custom，然后早Diff Command填入：`/usr/bin/bcompare` 在Arguments中填入：`$LOCAL $REMOTE`

  * 突破30天试用期方法：

    删除`/Users/michael/Library/Application Support/Beyond Compare/registry.dat`文件，或者参考https://blog.csdn.net/k12104/article/details/84104261中的方法

* DiffMerge

  * 安装方式：在终端中输入`brew install --cask diffmerge`
  * 在DiffMerge中配置中文UTF-8显示：
    * 打开DiffMerge
    * 菜单栏 - Preferences - File Windows - Rulesets
    * 进入Default Ruleset - Edit中Character Encodings中
    * Fallback Character Encoding Options中选择Use Named Encoding Below
    * 在Try Named Character Encodings中选择Unicode 8 bit (UTF-8)
  * 类似Beyond Compare的配置方式在SourceTree中配置DiffMerge作为文件比较合并工具

#### 在SourceTree中使用文件比较合并工具

在项目中点击文件，然后右键 - `Extern Diff` 或者 `Command` + `D`

