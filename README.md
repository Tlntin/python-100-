# 1.1版更新记录
1. 增加了一个python3在线运行网页
2. 暂时利用requests调用别人的接口，后期可能会使用沙箱环境自己搭建
# 说明
- 基于flask的一个小小小项目
- 题库来源已经标注，可看说明
- 使用的唯一依赖就是flask
```python
pip install flask
```
- 还有一个requests
```python
pip install requests
```
- 目前题库全部都是静态文件，后期可能考虑使用sqlite数据库储存题库与答案
- 然后用js脚本抽取数据简单评分
- 仅评兴趣，一个人录入比较累，项目可能会夭折
## 界面欣赏

![](http://vbahome.cn/img/深度截图_选择区域_20200522230154.png)

![](http://vbahome.cn/img/深度截图_选择区域_20200521233841.png)

![](http://vbahome.cn/img/深度截图_选择区域_20200521233849.png)

## 文件介绍
- main.py:运行的主文明件，运行后打开本地8002端口即可访问题库
- create.py：用于把大佬的题库连环问答生成单个问题与填空
- create2.py：功能同上，只不过上面与下面生成的样本不一样，可以自行观察代码
- static: 静态文件夹
- templates: 模板文件夹
## 题库录入方式
- 运行main.py文件，进入http://127.0.0.1:8082/
- 从templates文件夹，复制粘贴一个新html。比如117.html,117y.html复制为118.html,118y.html
- 进入大佬的题库http://127.0.0.1:8002/test/others/
- 将大佬的题目部分连环问题复制到create2.py中的text变量，然后运行create2.py
- 然后把刚刚create2.py输出的代码粘贴到html里面的问题区
- 然后把大佬题库里面的答案复制到答案区即可
- 顺便看看最上面的`<h1>``<h2>``<h3>``<p>`需不需要修改，可能还要添加一些code
## 作者说明
- 个人能力有限，开发暂时到这停止
- 有需要的自行录入一下后续题库，然后提交相关html文件即可
- qq交流群：974759263