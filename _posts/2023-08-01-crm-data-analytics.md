---
layout: post
title: CRM analysis and data governance architecture. | CRM分析以及数据治理架构
date: 2023-08-01 00:00:00
tags: Digital-Transformation CRM Data-Governance
categories: reflections
description: This is a reflection of how CRM helps better understand customers and how to do better data governance.
toc:
  sidebar: left
_styles: >
  ol {
    list-style-type: decimal;
    padding-left: 20px;
  }
  ul {
    list-style-type: disc;
    padding-left: 20px;
  }
  ol ul, ul ul {
    list-style-type: circle; /* or 'circle', 'square', 'decimal', etc. */
    padding-left: 40px;
  }
  ol ol, ul ol {
    list-style-type: decimal; /* or 'circle', 'square', 'decimal', etc. */
    padding-left: 40px;
  }
---
## English Version

### Data Analytics and CRM system

Data analysis typically refers to a broad range, from basic Excel, to data dashboards, to artificial intelligence and even intelligent decision-making. Traditional Customer Relationship Management (CRM) is more about managing relationships with B, C, G, and other end customers. However, with the popularity of e-commerce and online sales, especially in terms of data analysis and governance, CRM is more equated with membership management. It is about analyzing membership data to achieve refined operations of existing resources and further tapping into the value of the existing market. As the scale of the enterprise grows or market competition intensifies, the increasing cost of acquiring customers will inevitably lead companies to turn to the existing market to find new growth points.

**The purpose of the membership system in marketing, as I understand it, is as follows:**

* Increase average order value/repeat purchase frequency/total consumption.
* Create a sense of premium between members and non-members, and among different membership levels.
* Enhance customer loyalty and satisfaction, strengthen brand influence, and reinforce word-of-mouth.

**Some of the key steps involved typically include:**

* Collection of member data:
  * Basic data (personal information such as name, address, contact details, etc.)
  * Consumption data (details of each transaction)
  * Membership data (level, points, marketing)
* Establishment of the membership system:
  * Grading system (80/20 rule)
  * Points system (points in and out, realizing the value of points)
  * VIP system
* Implementation of touchpoint marketing:
  * Based on various information, provide exclusive marketing activities to members who meet certain criteria at specific times, places, and conditions, achieving refined operations and conversions.
  * Record the feedback of each member to marketing touchpoints.
  * Analyze, iterate, and retest the marketing plan based on data.

Regarding the effects that such a membership operation marketing system can achieve, I can use a very simple example. When applied to a large-scale member group, there will be differences, but the individual in the example actually represents a class of people. Therefore, the purpose and method of large-scale analysis are similar.

#### A small example

Ms. Yang likes to buy pies from the chain store at the entrance of her community when she gets off work. There's a reason she buys pies at this time, because after 6:30 pm, the seaweed pies are discounted.

For a CRM system, we can determine that Ms. Yang is price-sensitive but not taste-sensitive, using the following methods:

* Analyze Ms. Yang's past purchase records, comparing the number of discounted purchases to the total number of purchases, and the amount spent on discounted items to the total amount spent.
* Analyze the frequency and proportion of Ms. Yang's purchases during discount periods.

We can validate (promote, reach out, market) using the following methods:

* Issue Ms. Yang coupons for other products (new products) and record the coupon usage.
* Push referral promotions to Ms. Yang and record her social influence (to identify KOCs).
* Issue Ms. Yang high-value coupons with a high spending threshold to encourage her to increase purchase frequency/average order value.
* Etc.

Recently, Ms. Yang noticed that the chain store near her home launched a new braised flavor product. However, after purchasing it once, she did not repurchase. How can the CRM system determine if it's a. an issue with Ms. Yang personally, b. a pricing issue, or c. a quality issue with the braised product?
Prerequisites: 1. There has been a price-based A/B test for the new product launch. 2. Repurchase interval difference = the difference in time intervals between two consecutive repurchases.

* Check the repurchase interval difference in different price ranges of the A/B test. If it's independent of the price, then it's not a pricing issue.
* Check the repurchase interval difference in different stores. If it's independent of the store, then it's not a store issue (errors caused by individual stores).
* Compare the repurchase interval difference of other people with Ms. Yang's. If there's no difference, it's not an issue with Ms. Yang (more likely a product/quality issue).
* Otherwise, it's an issue specific to Ms. Yang. If she's a VIP customer, a targeted survey should be issued.

### Data Governance and Data Flow

The issue of data flow blockages is a common one. For instance, systems acquired from various companies might not effectively integrate and communicate data, leading to a plethora of derivative problems. I believe that the essence of data flow blockages is the uncertainty in data structure. This arises because, prior to advancing digitalization, there was no unified data standard across various sectors.

Each third-party company has its own understanding of the segment they are responsible for, and each interfacing sub-department has its own comprehension of its business. However, communication between third parties, as well as between departments, is not smooth. A single phenomenon or issue can be reflected through multiple indicators. Although they can corroborate each other, this leads to a situation where, during digitalization, different third parties or company departments might use different terms or logic to describe the same indicator. Taking a manufacturing enterprise's SAP system that I'm familiar with as an example: their entire SAP system is custom-developed. Whenever different individuals are responsible for the development of each financial segment, it results in poor interoperability between departments. Often, the same financial indicator has different calculation logic in different segments, leading to unnecessary errors and inaccuracies. Extending this issue to the company's entire SAP system follows the same logic. The underlying logic of each SAP subsystem should be consistent; otherwise, there will be a situation where each system speaks its own language.

In reality, the design of data flow and the SAP system should be quite intuitive. I believe:

* There needs to be a core indicator. This indicator should run through various stages of production and sales, representing a product. Typically, it's the product's SKU.
* Centered on this indicator, organize other data indicators from various departments surrounding it and determine the data format and dimensions.
* Based on the core indicator, establish data templates for each stage and test the data flow efficiency for each stage using these templates.
* After fully understanding the data, construct a comprehensive data system for various company segments and ensure its continuity.

## Chinese Version

### 数据分析和CRM

通常数据分析指代的范围广泛，从基础Excel，到数据看板，到人工智能乃至智慧决策都是数据分析。传统的客户关系管理（CRM）更多的是和B、C、G等各端客户之间的关系管理。但是在电商和线上销售火热的现在，尤其是在数据分析治理方面，更多的是将CRM和会员管理划等号，是通过分析会员的数据，来实现存量的精细化运营，是对于存量市场价值的进一步挖掘。随着企业规模的增大或者市场竞争的加剧，获客成本的增加势必会导致企业转向从存量市场中获得新的增长点。

**在营销中我所了解的会员系统的目的是这样的**

* 提升客单价/复购频次/总消费额
* 给会员与非会员，不同会员等级之间，制造出不同等级的心里尊贵感受
* 提高客户忠诚度和满意度，增强品牌影响力，强化口碑

**其中涉及到的一些关键的环节一般有**

* 会员数据的收集
  * 基础数据（姓名地址联系方式等个人信息）
  * 消费数据（每一笔消费详情）
  * 会员数据（等级、积分、营销）
* 会员体系的建立
  * 分级系统（2-8法则）
  * 积分系统（有出有进，落实积分价值）
  * VIP制度
* 触达营销的落实
  * 基于各种信息，在特定时间特定地点特定条件下，对满足一定条件的会员提供专属的营销活动，实现精细化运营和转化
  * 记录每个会员对于营销触达的反馈
  * 基于数据对当次的营销方案进行分析、迭代、再测试

关于这样的一套会员运营营销系统能达成的效果，我可以用一个非常简单的例子，实际应用于大规模会员群体时会有不同，但是例子中的个人实际是一类人群的代表，所以大规模分析时目的和方法是类似的。

#### 一个小例子

杨女士喜欢下班回家的时候在小区门口的连锁店买馅饼。她在这个时间买馅饼是有原因的，因为过了6点半以后海菜馅饼会打折。

对于一个CRM系统，我们是可以知道杨女士而她属于价格敏感，口味不敏感的人，方法如下：

* 分析杨女士在过去所有的购买记录中，折扣购买的次数与总次数、购买金额与总价格占比
* 分析杨女士在打折时间段的购买频次、购买金额的占比

我们可以用如下方法验证（推广、触达、营销）：

* 给杨女士发放其他产品（新产品）的优惠券，记录优惠券的消费情况
* 给杨女士推送好友裂变互动的推广，记录其社交影响力（可以找到KOC）
* 给杨女士发放大额优惠券但有高消费门槛，促使其提高消费频次/消费客单价
* 等

杨女士最近发现门口的连锁店推出了卤味新品，但是购买了一次以后没有产生复购，CRM系统要如何知道是 a.杨女士的个人问题 b.定价问题 c.卤味品质问题
前提：1. 新品上市至少有基于价格的A/B测试 2. 复购间隔差 = 连续两次复购的时间间隔的差值

* 查看AB测试中不同价格区间的复购间隔差，如果与价格独立，则不是定价问题
* 查看不同门店的复购间隔差，如果与门店独立，则不是门店问题（个别门店带来的误差）
* 查看其它人的复购间隔差与杨女士的差别，如果没有差别，说明不是杨女士的问题（更有可能是品质/产品的问题）
* 否则，是杨女士个人问题，如果是VIP客户，需要发放针对性的问卷进行调研。

### 数据治理和数据流

数据流不通畅的问题是一个常见的问题。例如从各个公司采买的系统之间不能很好的实现数据和互通整合，导致了很多衍生的问题。我认为数据流的不通畅本质上是数据结构的不确定。是在推进数字化之前，各部分的数据标准没有统一。

每个乙方公司都有自己对于他们负责的部分的理解，每个对接的子部门也都有自己对于自己业务的理解。但是乙方和乙方之间，部门和部门之间的相互沟通是不通畅的。一个现象或者问题是可以从多个指标中反映出来的，虽然他们可以相互印证，但是这导致了在数字化的时候，对于同一个指标，不同的乙方、不同的公司部门可能用不同的名词，不同的逻辑来描述。以我所了解的一个制造业企业的SAP系统为例，他们的整个SAP系统都是定制化开发的，但凡是财务中的每个部分的开发负责人不同，结果导致最后各个部门之间的互通性很差，往往同一个财务指标在不同的部分中的计算逻辑都不同，导致了很多不必要的误差和不精准。把这种问题扩展到整个公司的SAP系统也是同理。每个SAP子系统的底层逻辑应该是相同的，否则就会出现系统之间各各说各话的问题。

其实数据流和SAP系统的设计应该是比较直观，我认为

* 需要有一个最核心的指标。这个指标能够贯穿在生产销售各个环节，指代一个产品。通常为产品的SKU。
* 以这个指标为核心，整理各个部门围绕这个指标的其他数据指标，并确定数据格式和维度。
* 在核心指标的基础上建立各个环节的数据样表，依据这个样表尝试各个环节的数据通畅程度。
* 在充分理解数据的基础上，再去构建完整的，公司各个部分的数据系统并贯通。