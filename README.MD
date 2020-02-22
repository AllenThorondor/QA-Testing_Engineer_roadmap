## 写在前面

> 翻译自[anas-qa](https://github.com/anas-qa)/**[Quality-Assurance-Road-Map](https://github.com/anas-qa/Quality-Assurance-Road-Map)**，本人刚刚入行软件工程行业不久，才疏学浅，如有翻译的不对之处，欢迎指正。

# 简介💻

如果你立志成为一名软件测试工程师（QA engineer），以下内容可以帮到你，下面的内容是关于软件测试主要方面和技术要求的简洁介绍。

# 测试计划模版📚

完整的测试计划模版可以在测试计划模版.pdf 处浏览或者下载



```mermaid
graph TD
	start(基础部分)=="基本的学习曲线和助手"==>Testing_Strategy(测试策略)
	Testing_Strategy(测试策略)==>Testing_types(测试类型)
	Testing_types(测试类型)==>Test_Management(测试管理)
	Test_Management(测试管理)==>Tracking_Tools(跟踪工具)
	Tracking_Tools(跟踪工具)== 适应并学习SDLC模型 ==>development_methodologies(测试模型)
	
	subgraph testing_strategy
		Testing_Strategy(测试策略)-.-While_Box_Testing(白盒测试)
  	Testing_Strategy(测试策略)-.-Gray_Box_Testing(灰盒测试)
		Testing_Strategy(测试策略)-.-Black_Box_Testing(黑盒测试)
	end
	
	subgraph testing_type
		Testing_types(测试类型) -.- Functional(功能测试)
		Testing_types(测试类型) -.- NonFunctional(非功能测试)
	end
	
	subgraph test_management
		Test_Management(测试管理) -.- qTest(qTest)
		Test_Management(测试管理) -.- TestRail(TestRail)
		Test_Management(测试管理) -.- Zephyr(Zephyr)
		Test_Management(测试管理) -.- TestLink(TestLink)
	end
	
	subgraph tracking_tool
		Tracking_Tools(跟踪工具) -.- Assembla(Assembla)
		Tracking_Tools(跟踪工具) -.- Jira(Jira)
		Tracking_Tools(跟踪工具) -.- YouTrack(YouTrack)
		Tracking_Tools(跟踪工具) -.- Trello(Trello)
	end
	
	subgraph develop_method
		development_methodologies(测试模型) -.- V_Model(V模型)
		development_methodologies(测试模型) -.- Agile_Model(敏捷开发模型)
		development_methodologies(测试模型) -.- Waterfall_Model(瀑布模型)
	end
	
	

```

# 手动测试深度

1. 手动测试是任何软件测试的核心和基础，一个坚实丰富的基础会让你的职业生涯更加平稳
2. 做一个数据驱动的工程师可以节省你的时间，精力，让你有能力部署高质量而不是数量众多的测试案例

```mermaid
graph LR
TestPlaning[测试计划] -.- def_TestPlaning("规定测试活动的范围，方法，资源和进度；明确正在测试的项目，要测试的特性，要执行的测试任务，每个任务的负责人，以及与计划相关的风险")
TestCaseCreation[测试用例编写] -.- def_TestCaseCreation("测试用例是所有测试的基石，用例的编写基于功能的实现和用户的活动")
TestTypesUsage[测试类型选择] -.- def_TestTypeUsage("确定测试类型是测试工作的前提")
Reporting[测试报告] -.- def_Reporting("股东们都在看这个东西")
TroubleshootingSkills(问题解决技巧) -.- def_TroubleshootingSkills("寻找代码缺陷的根本原因")
STLC_in_SDLC(测试介入时机) -.- def_STL_in_SDLC("寻找合适的时机发布测试计划，不介入开发流程不影响开发进度，让开发和测试平滑进行")
Compatibility(共存性) -.- def_compatibility("为用户所有的场景负责，不忽视任何微小的缺陷")
Verification_Validation(验证和确认) -.- def_verification_validation("分清确认和验证的区别，验证是需求是否被满足(are we building the product in the right way)，确认是特定的目的是否被实现(Are we building the right product)")
TDD(TDD/测试驱动开发) -.- def_TDD("TDD是一个用完善的测试用例驱动开发过程，从而使得时间，精力，和测试周期大幅缩短的开发模式")
Risk_analysis(分险评估) -.- def_risk_analysis("分险评估非常重要")



```

# 自动化测试深度

```mermaid
graph TD
	
	Browsers_adds_ons(浏览器插件) ==> APIs_Automation(自动化API)
	
	subgraph "Recommended depth for Non Technical optional for Technical"
  Selenium(Selenium IDE) --- Ghost_Inspector(Ghost_Inspector)
  Ghost_Inspector(Ghost_Inspector) --- CodeCeption(CodeCeption)
	end
	
	Ghost_Inspector(Ghost_Inspector) --- Browsers_adds_ons(浏览器插件)
	
	subgraph tempTitle
  Protractor(Protractor) --- Robot_framework(Robot_framework)
	Robot_framework(Robot_framework) --- Cypress_io(Cypress.io)
	Cypress_io(Cypress.io) --- Codeception(Codeception)
	Codeception(Codeception) --- Rest_assured(Rest-assured)
		subgraph GUI
		PostMan(PostMan) --- SOAP_UI(SOAP UI)
		SOAP_UI(SOAP UI) --- RunScope(RunScope)
		end
		SOAP_UI(SOAP UI) --- Cypress_io(Cypress.io)
	end
	
	Codeception(Codeception) --- APIs_Automation(自动化API)
	Web&PWA_Automation(web或渐近式web程序) --- Elenments_Allocation(Elements Allocation)
	subgraph learn
		Selenium1(Selenium) --- Elenments_Allocation(Elements Allocation)
		Elenments_Allocation(Elements Allocation) --- Cypress_IO(Cypress.io)
	end
	
	APIs_Automation(自动化API) ==> Web&PWA_Automation(web或渐近式web程序) 
	
	Web&PWA_Automation(web或渐近式web程序) ==> web_Mobile_apps_Automation(web/Mobile Apps Automation)
	
	subgraph reactNative
		Appium(Appium) --- Detox(Detox)
		subgraph hands_on Emulator
			Macaca(Macaca)
		end
		Macaca(Macaca) --- Appium(Appium)
	end
	
	web_Mobile_apps_Automation(web/Mobile Apps Automation) --- Detox(Detox)
	
	subgraph headless browsers
		PHP_Browser(PHP Browser) --- Phantom_JS(Phantom JS)
		Phantom_JS(Phantom JS) --- Pupeteer_Chrome(Pupeteer Chrome)
		Pupeteer_Chrome(Pupeteer Chrome) --- Zombies_JS(Zombies JS)
	end
  web_Mobile_apps_Automation(web/Mobile Apps Automation) ==> Headless_browsers(Headless Browsers)
  Headless_browsers(Headless Browsers) --- Phantom_JS(Phantom JS)
  
  Git --- Jenkins(Jenkins)
  Jenkins(Jenkins) --- Github(Github)
  
  Headless_browsers(Headless Browsers) ==> Jenkins(Jenkins)
  
  subgraph Version Control
  	Git
  end
  
  subgraph CI & CD
  	Jenkins(Jenkins) --- GOCD(GOCD)
  end
  
  subgraph Reposotory Hosting
		Github(Github) --- Bitbucket(Bitbucket)  
  end
	
	
	
	
	
```

# 非功能性测试（负载&性能）

```mermaid
graph TD
	subgraph regular feedback regarding system scalability
	Load&Performance -- GUI Included -->JMeter
	Load&Performance -- CLI -->Vegeta
	end
```

# 建议

鼓励软件质量工程师确认合理的掌握了以上内容，而不是直接跳去学习自动化测试。因为自动化测试只不过是将手写的测试用例可读性，可理解性和重用性更好的手动测试罢了

# 执照

MIT