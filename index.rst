.. Ares documentation master file, created by
   sphinx-quickstart on Sun Oct 23 13:14:19 2011.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

==================
Ares 说明书
==================

介绍
============
:game:`Ares` 是一个 :game:`Yuri's Revenge` 的拓展其功能和修复其游戏引擎Bug的工具。
pd在2007年末构想了这一项目，并由 :doc:`The Ares Contributors </credits>` 开发数年。其首个版本发布于2010年。

本文档主要针对希望使用 :game:`Ares` 提供的新功能的模组作者。

:game:`Ares` 通过 :game:`Syringe` 与尤里的复仇共同使用。:game:`Syringe` 最初是由 pd 开发的，用于将 DLL 代码“注入”正在运行的应用程序中，而无需修改应用程序本身。

即，:game:`Ares` DLL 被注入到 :game:`Yuri's Revenge` 1.001 的主程序 :file:`gamemd.exe` 中。 支持正常升级的原始 CD 版本以及 :game:`The First Decade` 和 :game:`The Ultimate Collection` 的合集。

:game:`Syringe` 可以直接通过命令提示符运行，或通过 mod 提供的外部启动器运行。 更多详细信息，请参阅它们相应的文档。


内容
=================

.. toctree::
	:maxdepth: 1
	
	notes
	whatsnew
	migration

.. toctree::
	:maxdepth: 2
	
	bugfixes/index

.. toctree::
	:maxdepth: 3
	
	restored/index
	new/index
	ui-features/index
	
	comparison
	credits
	glossary

* :ref:`Overview of Ares's Bugfixes and Features <genindex>`
* :ref:`search`
