[Levels Ranks] Core 3.1
===========================

**[Levels Ranks] Core** - 一个统计插件，是RankMe、Sod Stats等类似统计插件的绝佳替代品。其核心很简单，执行各种游戏操作，会因此获得/失去经验值，当积累/失去一定数量的经验值时，会获得特定的等级。
统计学的种类：
----------------
- 累计型（lr_type_statistics 0）
 - 关键在于，你从最低等级开始，必须从0开始积累经验值。你玩得越多，等级就越高。
直接输出译文，不要解释，保证语义通顺：
- 评分类：：扩展（lr_type_statistics 1）
 - 这种统计类型类似于HlstatsX。其本质在于，你会获得平均等级和1000点经验值。而你的等级则取决于你的游戏技巧和表现如何。
直接输出译文，不要解释，保证语义通顺。
- 排名类::简单（lr_type_statistics 2）
 - 这种统计类型类似于RankMe。其本质与上述统计类型（扩展排名）相同，但在此类型中没有额外奖励，没有用于调整统计的乘数系数，而且此类型中采用的是另一种经验值计算公式。

支持的游戏：
--------------------
- CS: Source (v90/v34)
- CS: GO

前置：
-----------
- SourceMod <a href="//sourcemod.net/downloads.php?branch=stable">1.10.6422</a> и выше.

命令：
-------
- **sm_lvl** - 打开统计菜单。
- **sm_lvl_reload** - 重新加载插件的所有配置文件。
- **sm_lvl_reset** - 重置所有玩家的统计数据。
 - **all** - 将清除所有数据。
 - **exp** - 重置经验点数据（`value`，`rank`）。
 - **stats** - 重置统计数据（`击杀`、`死亡`、`射击`、`命中`、`头部射击`、`助攻`、`回合胜利`、`回合失败`）。
- **sm_lvl_del** - 重置特定玩家的统计数据。

安装：
---------

- 如果有，请删除插件的旧版本。

- 按文件夹解压内容。

- 设置文件：
	- addons/sourcemod/configs/databases.cfg
	- addons/sourcemod/configs/levels_ranks/settings.ini
	- addons/sourcemod/configs/levels_ranks/settings_ranks.ini
	- addons/sourcemod/configs/levels_ranks/settings_stats.ini​
	
- 重启服务器

配置 - databases.cfg
-------------------------

- 如果您打算使用SQLite数据库，则无需进行任何设置或添加。

- 如果您打算使用MySQL数据库，则需要将以下行添加到“addons/sourcemod/configs/databases.cfg”中，然后根据需要进行编辑：

```
	"levels_ranks"
	{
		"driver"	"mysql" 
		"host"		"host" 
		"database"	"database" 
		"user"		"login" 
		"pass"		"password"
	}
```
----------------------------------------------------------------------------------
