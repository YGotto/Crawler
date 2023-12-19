# Crawler
## 软工管网球垂直搜索引擎爬虫和写入elasticsearch
### crawler\data中存有爬取的数据：allPlayers.xlsx,allNews.xlsx,allMatch.xlsx,allVideos.xlsx
### crawler\src\main\java\org\example中为爬虫和elasticsearch操作的代码。
### 建立index并将数据写入本地elasticsearch流程：
1. 启动elasticsearch
2. 加载项目的maven依赖
3. 进入WriteMatch.java,将main函数第一行中writeBack中的参数改为allMatch.xlsx的绝对路径，运行WriteMatch
4. 进入WriteNews.java,将main函数第一行中writeBack中的参数改为allNews.xlsx的绝对路径，运行WriteNews
5. 进入WritePlayer.java,将main函数第一行中writeBack中的参数改为allPlayers.xlsx的绝对路径，运行WritePlayer
6. 进入WriteVideo.java,将main函数第一行中writeBack中的参数改为allVideos.xlsx的绝对路径，运行WriteVideo
### 写入elasticsearch后：
player中，选手最近比赛之间用#分隔，选手奖项之间用#分隔。

news中，正文部分用#代替了换行符。
