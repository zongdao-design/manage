[![Donate](http://www.zongdaosoft.com/static/index/images/logo.png)](http://www.zongdaosoft.com/)
# 模块测试要求
#### 作者：[RanChao]() 版本：[v1.0.0]()
### **软件测试**
软件测试（英语：Software Testing），描述一种用来促进鉴定软件的正确性、完整性、安全性和质量的过程。换句话说，软件测试是一种实际输出与预期输出之间的审核或者比较过程。软件测试的经典定义是：在规定的条件下对程序进行操作，以发现程序错误，衡量软件质量，并对其是否能满足设计要求进行评估的过程。
### **测试原则**
对计算机软件进行测试前，首先需遵循软件测试原则，即不完全原则的遵守。不完全原则即为若测试不完全、测试过程中涉及免疫性原则的部分较多，可对软件测试起到一定帮助。因软件测试因此类因素具有一定程度的免疫性，测试人员能够完成的测试内容与其免疫性成正比，若想使软件测试更为流畅、测试效果更为有效，首先需遵循此类原则，将此类原则贯穿整个开发流程，不断进行测试，而并非一次性全程测试。
### **目前现状及问题**
<b>现状：</b>  
1、开发和测试处于两条线，开发实现功能，测试确保开发实现功能是正常的。  
2、对于项目质量的保证工作都在开发编码完成后进行，虽然有时候可能开发完成一部分编码后测试就可以进行测试了。  
3、项目质量的保证完全由测试负责，开发只管实现功能。  
<b>问题：</b>  
1、测试介入时间较晚，bug修复成本大。  
2、开发提测的版本不稳定，Bug多，因为开发不对质量负责，开发自认为实现了功能或者说修改了bug，至于实现或者修复bug是否有影响开发并不关心，导致一个功能或者bug反复修改，反复测试，沟通成本高，容易导致项目延期。  
3、如果开发延期提交测试，测试时间被压缩， 项目上线质量不高，事实上，在产品过程中这种情况经常出现。  
4、测试和开发对立，开发认为测试做的都是低级工作却总是找自己麻烦，而测试觉得开会没有做好产品，代码质量低。

### **开发自检要求**
1、业务<b>功能</b>要求  
2、数据的<b>正确性</b>检查  
3、录入框的<b>容错性</b>控制和检查  
4、<b>特殊字符</b>的过滤和检查  
6、<b>数据有效性、边界值</b>控制和检查  
7、<b>设置字段、控件、数据</b>的默认值  
8、操作<b>方便性</b>、用户<b>体验</b>度、<b>人性化因素</b>等  
9、按照<b>不正常</b>的操作顺序去操作，看有无问题  
10、在一定数据量下的<b>稳定性</b>检查  
11、通过多录入一些数据，看<b>分页功能</b>有无问题  
12、要求模拟一定数据量，<b>检查性能</b>  
13、<b>当天任务</b>须由测试人员当天<b>测试并确认</b>  
14、<b>代码检查</b>，包括函数处理或SQL查询的<b>性能</b>、代码<b>逻辑性</b>、<b>注释</b>等  
15、接口文档是否按照[文档规范](https://github.com/zongdao-design/manage/blob/master/ApiDocStandard.md)编写