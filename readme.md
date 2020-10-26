模拟抽卡机器人。
包含各种热门游戏（等待添加）。
目前已经支持的有：
《原神》


基于 [YuQ](https://github.com/YuQWorks/YuQ) 开发。

#指令

```
XX十连
XX单抽

XX 为某个卡池的具体名字，直接替换带入即可。
```

#卡池阵容

```
《原神》
    常驻祈愿：
        奔行世间（原神）
    人物特定祈愿：
        闪耀的驻足（可莉）
    武器特定祈愿：
        神铸赋形 - 狼的末路&四风原典（狼末）
《明日方舟》
    待添加。
```
卡池后面的括号为指令用的卡池名。  
如模拟《原神》奔行世间祈愿，则指令为原神单抽，原神十连。

#结果解读

演示指令为：狼末十连
>@IceCream  
您的十连抽卡结果为：  
-- 蓝: 黎明神剑  
++ 紫: 祭礼剑 (保底) (大保底)   
-- 蓝: 飞天御剑  
-- 蓝: 铁影阔剑<br>
--------------------<br>
|| 金: 狼的末路 (26)  
--------------------<br>
-- 蓝: 神射手之誓  
-- 蓝: 沐浴龙血的剑  
-- 蓝: 黑缨枪  
-- 蓝: 以理服人  
-- 蓝: 魔导绪论  

```
在金色或者紫色的产出物后面，会跟随一个括号，括号内的内容可能为一个数字，或是保底。
数字则代表了这个产出物距离上次同等级产出物距离多少次抽卡。
保底则是代表了，触发了保底。

大保底则是代表了本次奖励触发 UP 池，第二次必出当期 up 的结果。
四星和五星的大保底是独立计算。
四星也是有大保底的。

为了方便计算，在不同期的 up 池中，抽卡数据不互通。
即，模拟情况下，进行温迪十连八次无金色产出物，再进行一次可莉十连不会触发 90 次保底。
```
 
#食用方法

```
clone。
编辑 ./src/main/resource/conf/bot.properties。
填写 QQ 账号与 QQ 密码。
./gradlew build
java -jar ./build/libs/YuanShenBot-1.0-SNAPSHOT-all.jar
```

#卡池添加

后续会继续添加各种游戏的卡池。  
欢迎提供各个游戏的抽卡方式以及卡池数据。  

#免责声明

```
机器人所涉及的所有抽卡几率均为游戏运营商官方公示数据。
机器人卡池内容版权及著作权属于《原神》官方。
机器人卡池内容版权及著作权属于源版权所有方，机器人仅对其进行收集。
模拟抽卡数据仅供参考娱乐，作者对任何使用者不承担任何责任。
```