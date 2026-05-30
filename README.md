[Levels Ranks] Core 3.1
===========================

**[Levels Ranks] Core** - 这是一个统计插件，对于您来说，它是RankMe、Sod Stats等类似统计插件的绝佳替代品。其核心很简单，您执行各种游戏操作，会因此获得/失去经验值，当积累/失去一定数量的经验值时，您会获得特定的等级。
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

Поддерживаемые игры:
--------------------
- CS: Source (v90/v34)
- CS: GO

Требования:
-----------
- SourceMod <a href="//sourcemod.net/downloads.php?branch=stable">1.10.6422</a> и выше.

Команды:
-------
- **sm_lvl** - открывает главное меню статистики.
- **sm_lvl_reload** - перезагружает все конфигурационные файлы плагина.
- **sm_lvl_reset** - сбрасывает статистику у всех игроков.
	- **all** - сбросит все данные.
	- **exp** - сбросит данные о очках опыта (`value`, `rank`).
	- **stats** - сбросит данные о статистике (`kills`, `deaths`, `shoots`, `hits`, `headshots`, `assists`, `round_win`, `round_lose`).
- **sm_lvl_del** - сбрасывает статистику у конкретного игрока.

Установка:
---------

- Удалите прошлую версию плагина, если есть.

- Распакуйте содержимое по папкам.

- Настройте файлы:
	- addons/sourcemod/configs/databases.cfg
	- addons/sourcemod/configs/levels_ranks/settings.ini
	- addons/sourcemod/configs/levels_ranks/settings_ranks.ini
	- addons/sourcemod/configs/levels_ranks/settings_stats.ini​
	
- Перезапустить сервер

Настройка - databases.cfg
-------------------------

- Если вы собираетесь использовать БД SQLite, то ничего не нужно настраивать и добавлять.

- Если вы собираетесь использовать БД MySQL, то вы должны добавить строки, которые даны ниже, в "addons/sourcemod/configs/databases.cfg", а затем отредактировать как вам требуется:

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

<a href="//discord.gg/Jc58wjF">Официальный Discord-канал поддержки Levels Ranks</a>
