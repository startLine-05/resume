<h1>
  <span>前端开发</span>
  <span>李铁英</span> <br>
  <ul>
    <li><span>性别</span>男</li>
    <li><span>学历</span>全日制统招本科</li>
    <li><span>电话/微信</span>18223255443</li>
    <li><span>邮箱</span>startline_05@163.com</li>
    <li><span>博客</span><a href="https://salted_fish_machine_05.gitee.io/start-line-blog">https://salted_fish_machine_05.gitee.io/start-line-blog</a></li>
  </ul>
</h1>

## 工作经历

**华为 OD-PLM 开源漏洞与系统设计-ASD 系统设计团队 软件开发岗（前端）**<span class="right">2022.7 - 至今</span><br>

- 1.负责全量分析系统的代码仓 monorepo 化和项目重构，项目的流水线搭建和代码分支管理与代码 review
- 2.负责项目部分 US 录入,Task 拆分,技术选型（如微前端，多系统通信交互设计）和整体业务流程把控
- 3.负责项目规范化方案设计和性能优化落地等，并组织分享技术/框架赋能
- 4.华为<a href="https://github.com/DevCloudFE">DevUI Design</a>（内源/开源）贡献者（build 模块田主）

**恒生云融公司（B 轮）- 信贷产品线 软件开发岗（前端）**<span class="right">2021.7 - 2022.7</span><br>

- 1.负责现场的前端管理和公司中台业务对接。
- 2.负责现场前端项目需求分析和整体业务流程把控。
  <br/>

**文达智通公司-产品赋能部门 前端开发岗**<span class="right">2019.10 - 2021.7（含实习）</span><br>

- 1.负责全套小程序端开发/重构，负责 SaaS 系统的开发。
- 2.负责前端技术选型,需求评审，原型评审，代码仓管理/代码审查等。
  <br/>

## 技术栈

- <b>基础：</b>熟悉 Html5,Css3 新特性， 扎实的 JavaScript/TypeScript/Es6 语法基础。
- <b>PC 框架：</b> 熟悉 Vue3/Vue2 、React 全家桶， 熟悉 wujie(腾讯)，ice（阿里）等微前端框架。熟悉常见的 UI 库。
- <b>移动端框架(Hybrid 跨端):</b> 熟悉 Uni (基于 Vue 语法和小程序接口)跨平台框架，小程序 H5 等。
- <b>工程化:</b> 熟悉基于 pnpm 的 monorepo 单一代码库架构、熟悉基于多系统组合的 MicroService 微服务架构 、熟悉 node 项目搭建=>基于 vite/rollup 打包=>自动化测试/部署=>持续集成。具有 JS 库，组件库等搭建/编写能力。
- <b>规范：</b>ESLint 代码规范，commit 提交规范, vue 风格指南,具有面向类型、模块化、抽象的编程习惯。
- <b>研发流程：</b>熟悉 git 代码分支管理/检视。熟悉基于 CI/CD、DevOps 项目持续化集成与产品开发流程管理。
- <b>其他：</b> 熟悉前后端交互，浏览器/网络/性能调试，对后端接口以及表结构有一定认知。熟悉常见的性能分析与优化、熟悉常见的数据结构/算法/设计模式。

## 项目经验

### **全量分析系统 Web 平台**

#### **项目描述**：

该项目是由 wujie 微前端 + monorepo 架构搭建的需求分析作业平台，(目前接通云核/终端/光/车 Bu/能源等产品线) 主要针对于需求 SE/产品架构师使用，帮助用户分析需求，并且建立需求文档，实现设计作业。

#### 技术选型：Vue3 + TypeScript + wujie + monorepo + DevUI

#### 负责内容：

- 负责全量分析项目项目重构/技术选型，以及资产作业页面开发。
- 负责全量分析左树开发，以及作业页面数据注入/通信等。

#### 部分架构难点：

- **简介**：需求分析平台由编排服务、文档模板管理、全量分析服务、功能库服务等子模块组成的需求分析平台。平台主要有左树以及右侧编排作业内容构成。编排服务用于构建左树节点和配置转发配置页面，文档模板管理用于组装配置文档。
- **通信**：多系统之间通过 wuJie 微前端和 iframe 嵌套接入的背景，因此制定制定的标准的通信内容和通信(postMessage)，并通过单列，抽象工厂，观察者等设计模式封装一套事件冒泡通信库，用于打通多层次系统嵌套通信。
- **左树**：左侧节点采用双向链表树结构，降低树查找性能（如节点跳转）。采用虚拟渲染/懒加载方法保证上万条节点渲染性能。并且通过封装抽象类实现节点数据组装并注入右侧作业内容。
- **架构**：使用基于 pnpm 的 monorepo 架构重构代码仓目录，将中大型项目拆解成多个子项目，使多团队开发同时互不影响。借助 pnpm-workspace 能力，让多项目解除耦合的同时实现代码共享。重构后的架构提高了构建速度（30~40%）/项目访问速度（11%），减小项目之间耦合，大大提高代码的可维护性。
- **其他**：使用 Tsx 封装 DevUi 组件，并且提供更好类型推断。编写插件方法结合 wujie 暴露钩子和使用 nginx 等,解决微前端一些兼容性疑难杂症（如下拉框错位，获取不到浏览器事件对象,跨域等）。

---

### **云融信贷 3.0 平台**

#### **项目描述**：

该项目是由微前端 + 分布式微服务构建的大型信贷系统。他包含小微金融系统，后台管理系统等数十余个系统。客户通过上架对应借贷产品，配置审批节点，配合后台自动核算，跑批完成一系列借贷流程。

#### 技术选型：React + Antd + yrAntd（云融公司组件） + ice + iceStark (微前端)

#### 负责内容：

- 完成税 e 贷，兴农贷，收银 e 贷，公积金贷等混合应用独立开发。
- 维护其他标准产品，和对接中台/其他平台系统。

#### 部分技术架构：

- **路由**：微前端分解耦各个系统，子应用动态部署注册后，将路由并传递给后端进行路由合并后返给基座，基座对路由进行分拨对应权限，控制子应用/混合应用间跳转，实现可插拔的动态路由与个性化页面。
- **共享**：子应用间采用全局变量，Session Storage，路由变量，实现数据共享或传递。子应用通过 store 管理当前应用数据。
- **权限**：前端使用 node 脚本遍历 router(路由菜单)，serve（接口请求）,virtual-group（虚拟权限组），文件生成 oracle_sql 并连接数据库插入对应权限，前端校验后渲染对应菜单，区块，或请求对应接口。
- **插件**：使用 node（child_process）获取 git 分支，版本，应用配置等信息，通过 webpack 制作 plugin 打印信息插件，能在线上环境打印出应用信息，方便定位问题。

---

### 文达智慧案场小程序

#### 项目描述：

本项目属于 Hybrid 模式开发，小程序为系统数据主入口，文达（中心+报备+接待+巡检+AI 语音管家）小程序，主要为经纪人对顾客进行数据报备和职业顾问签到接待等，并且为 sass 系统提供数据主入口。

#### 技术选型：**Vue + Uni + uview + BLE（低功耗蓝牙） + 微信小程序 wxs + uCharts 等**

#### 负责内容：

- 参与全套小程序的重构与维护，从页面设计到功能实现均独立完成。

#### 难点内容：文达 AI 语言官家微信小程序

- 核心为音频详情界面，由于小程序隔离了渲染进程和逻辑进程，为了防止进程阻塞，采用栈/事件循环分批更新数据，实现上千条对话数据渲染同时页面不卡顿。
- 通过节流实现音频条流畅拖动，并通过复杂计算实现对话定位，关键词命中等。
- 通过 ArrayBuffer 传输二进制数据实现与录音笔通信,使用队列数据结构解决指令集冲突问题,使用边广播边解析和直连解决 IOS 与安卓的蓝牙设备 ID 不一致问题。
  采用工厂/单列模式，封装蓝牙类挂载于 store，大大提高代码的可维护性（另附自制开源蓝牙调试工具详见简历下方）。

---

<br>

## 开源项目与视野

**git 和 github 共累计 50+ Stars，开源库 dev-ui 、uview 贡献者**

- gitee:<a href="https://gitee.com/salted_fish_machine_05">https://gitee.com/salted_fish_machine_05</a>
- gitHub:<a href="https://github.com/startLine-05">https://github.com/startLine-05</a>

**开源项目**

- <a href="https://gitee.com/salted_fish_machine_05/uni-app-wangyiyun">仿网易云音乐 APP（大学时期开发） (uni + node.js github 开源接口)</a>
- <a href="https://github.com/startLine-05/startline-caricature-client">startLine 漫画 + 管理台 + 云后端（云存储，云函数）</a>
- <a href="https://github.com/startLine-05/uni-BLE">BLE 蓝牙调试工具 (uni + BLE)</a>

- 其余知乎，掘金，开源项目等链接可访问<a href="https://salted_fish_machine_05.gitee.io/start-line-blog">个人博客 </a>(持续更新)或<a href="https://github.com/startLine-05">github</a> 查看

---

<br>

## 自我评价

- 开源爱好者，源码阅读者，有良好的自驱动性，对互联网 web 端有浓烈的兴趣和进阶学习的动力。
- 有良好的代码规范，有注释习惯，代码洁癖，模块面向对象的封装思想。
- 有良好的团队精神和协同能力，能够快速融入团队。
