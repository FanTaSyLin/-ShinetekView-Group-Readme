# ShinetekView的规划与说明

ShinetekView是一个遥感卫星产品集成显示平台，支持多源、多尺度、多形态的气象数据和卫星遥感数据的发布与展示。为用户提供交互式的图像浏览与分析体验。

ShinetekView包括以下应用与服务：

## 目录

* [概述](#概述)
* [管理规范](#管理规范)

## 概述

ShinetekView包括以下系统与服务:

* **Application**
  * ShinetekView-EMAMS - 生态气象监测与评估系统（Ecological meteorological assessment and monitoring system）
  * ShinetekView-MEROS - 气象遥感观测系统（Meteorological Remote-Sensing Observation System）
  * ShinetekView-ENROS - 环境遥感观测系统 (Environment Remote-Sensing Observation System)
  * ShinetekView-ISRAS - 行业专项遥感数据分析系统集 (Industry special remote sensing data analysis system)
    * firemonitor - 火情监测软件
    * 。。。。
* **Microserver**
  * Service-Snipshot - 截图服务
  * Service-Events - 事件服务
  * Service-Thematic - 专题图制作服务
  * Service-PointValue - 屏幕取值服务
  * Service-StaticServe - 静态文件获取服务
  * ... ...

### Application

#### **ShinetekView-EMAMS**

> 生态气象监测与评估系统（Ecological meteorological assessment and monitoring system）

#### **ShinetekView-MEROS**

> 气象遥感观测系统（Meteorological Remote-Sensing Observation System）

#### **ShinetekView-ENROS**

> 环境遥感观测系统 (Environment Remote-Sensing Observation System)

### **ShinetekView-ISRAS**

> 行业专项遥感数据分析系统 (Industry special remote sensing data analysis system)

### Microservice

#### Service-Published

> 遥感产品发布服务

包括以下API:

* 目录服务
* 图像发布服务
* 动画服务
* 调色板服务

[详情请见](./doc/service-published.md)
[返回顶层](#目录)

## 管理规范

> 本规范旨在对ShinetekView平台下的系列应用与服务进行统一设计，使其具备统一的开发标准。为日后的集成、扩展、部署、运维等工作提供一致性操作。

### 命名规范

* Application命名统一使用ShinetekView + 5位大写英文缩写 如:
  * ShinetekView-EMAMS
  * ShinetekView-MEROS
* Microservice命名统一使用ShinetekService + 服务名(骆驼式命名) 如:
  * Service-ScreenShot
  * Service-ThematicMap

### 端口管理

* Application 使用4500 ~ 4599
* MicroServer 使用4600 ~ 4799

具体分配详见: [端口号分配表](./doc/shinetekview-port-table.md)

### 部署与配置项管理
