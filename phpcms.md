#phpcms介绍
##(1)phpcms安装
	1)需要下载一个phpcms的安装包
	2)安装phpcms这个项目
##(2)一些简单的配置
	1)删除一个index.html文件
##(3)phpcms的介绍
	1)相关目录的介绍
		m model
		v templates
		c modules
		公共类库：libs
		多语言：languages
		插件：plugin
##(4)内容->栏目->模型
	管理内容：为我们的栏目添加内容
	管理栏目：为我们的导航添加栏目
	模型管理：为我们栏目定义表(这个表就是栏目后期进行数据增删改查的表)
##(5)自个新建一个自个的模板
	1)自个新建了一个模板了
	2)替换成为我们自个新建的一个模板呢？
		需要把管理栏目中的模板设置成为站点修改的模板
##(6)替换模板
	1)公共资源配置文件
		\caches\configs\system.php
		\caches\configs\route.php    //首次访问地址
	2)添加一个化共的资源路径
		\install_package\caches\configs\system.php //先定义一个路径
		\install_package\phpcms\base.php           //定义一个常量，这样子模板中就可以调用这个常量的值
##(7)模板内容替换
	1)
	{loop $data $n $r}：循环，相当于foreach($dataas $n=>$r)
	{if!empty($SEO[‘title’])}{$SEO[‘title’]}{/if}：判断结构
	{template‘content’ , ‘left’ , ‘public’}：模板加载，相当于 include(‘templates/public/content/left’)  {php }：php标签，相当于<?php ?>
	{$r[‘url’]}：输出，相当于echo$r[‘url’]

##(8)需要做的
	1)首页信息替换成动态的
	2)列表页信息需要替换成为动态的
	3)详情页信息需要替换动态的


		
