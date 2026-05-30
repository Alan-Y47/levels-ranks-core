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

<details><summary>Скриншоты</summary>
<p>
	<a href="//levels-ranks.ru/content/core/MainMenu.jpg"><img src="https://levels-ranks.ru/content/core/MainMenu.jpg"/></a>
	<a href="//levels-ranks.ru/content/core/MenuMyStats.jpg"><img src="https://levels-ranks.ru/content/core/MenuMyStats.jpg"/></a>
	<a href="//levels-ranks.ru/content/core/MenuMySession.jpg"><img src="https://levels-ranks.ru/content/core/MenuMySession.jpg"/></a>
	<a href="//levels-ranks.ru/content/core/MenuResetStats.jpg"><img src="https://levels-ranks.ru/content/core/MenuResetStats.jpg"/></a>
	<a href="//levels-ranks.ru/content/core/MemuInventory.jpg"><img src="https://levels-ranks.ru/content/core/MemuInventory.jpg"/></a>
	<a href="//levels-ranks.ru/content/core/MenuTop.jpg"><img src="https://levels-ranks.ru/content/core/MenuTop.jpg"/></a>
	<a href="//levels-ranks.ru/content/core/MenuTop.jpg"><img src="https://levels-ranks.ru/content/core/MenuTopPoints.jpg"/></a>
	<a href="//levels-ranks.ru/content/core/MenuTop.jpg"><img src="https://levels-ranks.ru/content/core/MenuTopActivity.jpg"/></a>
	<a href="//levels-ranks.ru/content/core/MenuTop.jpg"><img src="https://levels-ranks.ru/content/core/MenuRanks.jpg"/></a>
	<a href="//levels-ranks.ru/content/core/ChatRankStats.jpg"><img src="https://levels-ranks.ru/content/core/ChatRankStats.jpg"/></a>
</p>
</details>

支持的游戏：
--------------------
- CS: Source (v90/v34)
- CS: GO

前置：
-----------
- SourceMod <a href="//sourcemod.net/downloads.php?branch=stable">1.10.6422</a> и выше.

命令：
-------
- **sm_lvl** - открывает главное меню статистики.
- **sm_lvl_reload** - перезагружает все конфигурационные файлы плагина.
- **sm_lvl_reset** - сбрасывает статистику у всех игроков.
	- **all** - сбросит все данные.
	- **exp** - сбросит данные о очках опыта (`value`, `rank`).
	- **stats** - сбросит данные о статистике (`kills`, `deaths`, `shoots`, `hits`, `headshots`, `assists`, `round_win`, `round_lose`).
- **sm_lvl_del** - сбрасывает статистику у конкретного игрока.

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
