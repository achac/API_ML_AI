## Product requirements
Target relese     |    2018/12/01
----------------- |    -------- 
Ecip | 账单助手APP
Document status | 进行中
Document onwer | 谢汐
Designer | 谢汐
Develope | 谢汐
QA | 谢汐

## 加值宣言
运用百度AI中图像技术里的文字识别中的通用票据识别技术，能够在账单助手APP中优化记账方式，将消费票据中的信息识别出来，按行返回识别结果，APP后台根据返回结果对消费内容进行分类，并储存为电子账单，形成账单电子化。

## 核心价值
核心价值宣言：实现一个有识别票据功能的记账APP,在基础的记账功能上增加识别消费票据功能，并做好分类储存。包括购物小票、增值税发票、医疗账单、车票等，都可通过扫描或者上传从而将其储存为电子版，APP可根据扫描结果进行分类，再加其加入账单的消费明细中，形成电子化账单。

## 需求列表与人工智能API加值


## 核心价值与用户痛点
* 在记账过程中整理消费票据时需要手动一项一项输入金额与消费类别，才会形成账单。
* 日常消费的票据种类过多，不易整理与保存。
* 

## 人工智能概率性与用户痛点
* 在识别超市类小票时的准确度较高，但个别地方仍存在错误。
![消费票据](http://img.piaoliang.com/uploads/allimg/130912/1529215S6-0.png)

![识别结果](https://bdn.135editor.com/files/users/150/1501074/201812/pV8JXgju_43Y4.png)
* 在识别车票时，对于金额的识别比较准确，但对证件号的识别会出现一些疏漏。
![车票识别](https://bdn.135editor.com/files/users/150/1501074/201812/HuRCgfIv_BzFR.png)

* 在对消费票据进行识别的过程中，个别地方仍存在错误，但整体识别较为准确，在主要内容的识别上准确度较高。



## Goals
* 简化个人账单记录方式，提供便捷记账功能
* 运用文字识别技术，实现购物小票与发票电子化储存，用户扫描或上传购物小票或发票，可转换为电子格式，便于储存与分类
* 分类管理账单，记录各方面支出情况，统计分析支出
* 自定义账单标签，在原有的标签上可根据用户需求自行添加新的标签类目


## Background and strategic fit
记账是许多人的习惯之一，能清晰的了解并管理自己的支出情况。在日常记账中，购物小票或需要整理的发票总是不太好处理，用户要手动添加进他们的账单里，而运用文字识别，将其电子化储存便方便了许多，既能实现记账又能将其转换为电子账单。

## Assumptions
用户在使用此主要功能时，主要是在使用手机的情境下。

## Requirements
* 管理日常购物的小票，将其转换为电子版记录在账单，无需自己手动输入
* 整理纸质版发票，将其转换为电子版保存
* 记录自己的消费情况，以便了解自己的支出状况
* 清楚的知道自己的财务情况，及时调整或控制自己的消费
* 将琐碎零散的消费记录分类管理，汇总整理成图表，可以清楚的看到自己在各个分类的消费
* 可自定义账单标签，根据不同需求进行增加或删除

## The target user
* 有记账习惯的人群
* 日常需要整理保存发票的群体
* 生活有条理，爱好整理的群体
* 收入水平较低的学生群体
* 常在超市、便利店消费的群体
* 喜欢记录生活的群体

## The content range
#### 识别票据
用户可通过直接对票据进行拍照或从手机里上传票据照片，则会将票据转换为与图片一致的文字电子版，用户可自行为其添加标签进行分类，后台对识别结果中的金额参数进行提取，将其放入账单明细中，这一项支出则会被记录到用户选择的账单类目里面，并在账单明细中显示。
#### 记账明细
记录自己的收支情况，用户可自行添加收入或支出的金额，可对其进行时间、类目上的选择，可对所记录的每笔账添加备注，保存后便会以明细的形式呈现。收入会以正数形式呈现，支出则以负数形式呈现。在页面上显示的明细由时间顺序排序，日期最近的支出在最前面。
#### 发票整理
用户对发票进行拍照或上传发票照片，都会转换为电子发票，并单独放在一个地方保存，以供用户可单独查看电子发票。
#### 自定义账单类目
用户可在原有的类目上自行增加或减少支出或收入类目，自定义账单类目。
#### 分析统计账单
根据用户的记账明细与分类，统计出一个时间区间的各个类别的支出，以图表形式呈现，账单统计按金额由高至低排序，用户可选择时间或类别查看账单总金额，对自己该阶段的支出能有一个清楚的认知。
#### 账户管理
当用户输入收入与支出后，会根据用户记录的支出显示余额，便于用户查看自己账户资金。

## User interaction and design 
![架构](https://bdn.135editor.com/files/users/150/1501074/201811/RvkN4f5S_Zwcc.png)
#### [产品原型](https://achac.github.io/bill-assitant/)


## 文字识别API调用
* 用户对票据拍照或上传票据照片
* 使用百度AI中的[票据识别](http://ai.baidu.com/tech/ocr/receipt)技术，识别图片中的文字
* 返回识别参数，生成识别结果

## Questions
* 解决购物小票杂乱、不好整理收纳的问题
* 解决零散的账单的分类问题
* 解决不清楚或忘记自己支出状况的问题

## Not doing
不置入广告，不给用户推荐理财产品等广告信息。

## 清单
产品原型：https://achac.github.io/bill-assitant/

票据识别：http://ai.baidu.com/tech/ocr/receipt

