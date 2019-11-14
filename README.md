![CLEVER DATA GIT REPO](https://raw.githubusercontent.com/LiCongMingDeShujuku/git-resources/master/0-clever-data-github.png "李聪明的数据库")

# 打破8192字符限制在SQL
### Break the 8192 Character Limit in SQL
**发布-日期: 2014年05月01日 (评论)**

## Contents

- [中文](#中文)
- [English](#English)
- [SQL Logic](#Logic)
- [Build Info](#Build-Info)
- [Author](#Author)
- [License](#License) 


## 中文

有时你会遇到SSMS文本输出中没有足够字符的情况。幸好，有一个快捷的办法帮助你（在TSQL中），你不必通过SSMS GUI或CTRL + T将结果设置为文本输出。

你只需在语句末尾添加一行。

你可以在任何声明后执行此操作，并查看你获得的结果类型。它们将显示在另一个标签中。这么做你将获得XML语法。但还有另一种方式执行此操作（如下）。

## English
Occassionaly you’ll run into a point where you aren’t getting enough characters in the Text output of SSMS. Fortunately; there’s a quick thing you can do (within TSQL), and you don’t have to mess around with setting the results to Text Output either through the SSMS GUI, or CTRL+T.

You simply add a single line at the end of your statement.

You can do this after any statement and see what kind of results you get. They will be displayed in another Tab. You’ll get the XML syntax with that but there’s another way you can do it below.


例如（Example）



---
## Logic
```SQL
use master;
set nocount on
select
	name
from
	sys.databases
for 
	xml path(''), type

```

![#](images/8192-character-limit-1.png?raw=true '#') 

或者，如果你希望结果是直接文本而没有所有XML语法（你可以简单地复制并粘贴到其他内容中），你可以将结果放入变量中，并选择变量SELECT @MyVariable，xml路径将在单击链接后仅列出文本。就像这样。


Or… If you want the results in straight text without all the XML syntax ( that you can simply copy and paste into something else ), you can put the results into a variable, and select the variable SELECT @MyVariable, and the xml path will list only text after you click on the link. Like so…

![#](images/8192-character-limit-2.png?raw=true '#') 

---

[![WorksEveryTime](https://forthebadge.com/images/badges/60-percent-of-the-time-works-every-time.svg)](https://shitday.de/)

## Build-Info

| Build Quality | Build History |
|--|--|
|<table><tr><td>[![Build-Status](https://ci.appveyor.com/api/projects/status/pjxh5g91jpbh7t84?svg?style=flat-square)](#)</td></tr><tr><td>[![Coverage](https://coveralls.io/repos/github/tygerbytes/ResourceFitness/badge.svg?style=flat-square)](#)</td></tr><tr><td>[![Nuget](https://img.shields.io/nuget/v/TW.Resfit.Core.svg?style=flat-square)](#)</td></tr></table>|<table><tr><td>[![Build history](https://buildstats.info/appveyor/chart/tygerbytes/resourcefitness)](#)</td></tr></table>|

## Author

- **李聪明的数据库 Lee's Clever Data**
- **Mike的数据库宝典 Mikes Database Collection**
- **李聪明的数据库** "Lee Songming"

[![Gist](https://img.shields.io/badge/Gist-李聪明的数据库-<COLOR>.svg)](https://gist.github.com/congmingshuju)
[![Twitter](https://img.shields.io/badge/Twitter-mike的数据库宝典-<COLOR>.svg)](https://twitter.com/mikesdatawork?lang=en)
[![Wordpress](https://img.shields.io/badge/Wordpress-mike的数据库宝典-<COLOR>.svg)](https://mikesdatawork.wordpress.com/)

---
## License
[![LicenseCCSA](https://img.shields.io/badge/License-CreativeCommonsSA-<COLOR>.svg)](https://creativecommons.org/share-your-work/licensing-types-examples/)

![Lee Songming](https://raw.githubusercontent.com/LiCongMingDeShujuku/git-resources/master/1-clever-data-github.png "李聪明的数据库")

