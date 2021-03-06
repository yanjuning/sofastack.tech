---
title: "让 AI 无处不在：滴滴与蚂蚁金服开源共建 SQLFlow"
author: "SQLFlow"
authorlink: "https://sqlflow.org"
description: "让AI 像 SQL 查询一样简单。"
categories: "SQLFlow"
tags: ["SQLFlow"]
date: 2019-09-29T15:00:00+08:00
cover: "https://cdn.nlark.com/yuque/0/2019/jpeg/226702/1569749289197-4c3f02bc-28f4-49fe-9499-38c55a2e542d.jpeg"
---

2018 年 1 月，Oracle 的官方博客上发表了一篇文章，标题是“It's Pervasive：AI Is Everywhere”。作为全球最著名的商业数据库系统提供商，Oracle 在这篇文章里历数了 AI 在企业信息系统中的发展空间。在面向最终用户的互联网行业，巨头们招募 AI 专家，用 Python 和 C++ 打造服务大众的特定 AI 能力——搜索、推荐、以及精准定向的互联网广告系统。在企业业务中，使用 SQL 的分析师是大多数。

![滴滴首席数据科学家谢梁（左）与蚂蚁金服研究员王益开启共建SQLFlow之旅](https://cdn.nlark.com/yuque/0/2019/png/226702/1569746168256-0021b8db-3680-4ee1-bcfe-bc5f6e98a9ee.png)

滴滴首席数据科学家谢梁（左）与蚂蚁金服研究员王益开启共建SQLFlow之旅

2019 年 7 月，滴滴的数据科学（Data Science）团队的几名数据科学家在北京新澄海大厦见到了来自蚂蚁金服的几位工程师。在那之前两个月，蚂蚁金服从事 AI 基础架构研发的王益团队开源了一款机器学习工具 SQLFLow，将 SQL 程序翻译成 Python 程序，调用数据库和 AI 引擎，实现端到端的 AI。滴滴首席数据科学家谢梁敏锐地关注到这个项目。这次拜访双方一拍即合，开启了共建 SQLFlow 之旅。

![](https://cdn.nlark.com/yuque/0/2019/gif/226702/1569745868527-966525c1-7034-4b1a-a428-20645a770e00.gif)

用 SQLFlow 构建 AI 的训练和预测任务

### 数据分析师的普适 AI 

数据驱动决策是很多公司的追求，在国内很多业务人员都了解 SQL，但是对于 AI、深度学习模型的训练，需要长时间系统性的学习，有一定的门槛。SQLFLow 的出现让包括数据分析师在内的业务人员通过写简单的 SQL 去调用 AI 模型成为了可能。滴滴数据科学团队长期地直面一线业务，了解业务需求，也沉淀了很多常用模型。本次合作双方希望优势互补共同助力 AI 的落地，据悉合作分为三步，第一步滴滴为蚂蚁金服贡献更多针对于业务产品的理解和洞见；第二步滴滴将公司自身业务场景最有价值用的最好的模型贡献到 SQLFLow；第三步滴滴加入到建设到整个 SQLFLow 开源社区的建设，双方要在模型、社区、文化等全方位共建。

![SQLFlow的技术架构](https://cdn.nlark.com/yuque/0/2019/png/226702/1569746422518-538c9048-9fb9-427f-83c1-1e6d21d4fc7b.png)

SQLFlow的技术架构

一个多月的时间，滴滴已经为 SQLFLow 贡献了基于 DNN 分类预测模型、可解释模型和无监督聚类模型三个高价值模型。这三个模型覆盖的场景非常广泛，对于滴滴内部来说，包括网约车、单车、金融等在内的诸多业务场景都可应用起来，于外部而言，“因为整个模型它是一种基础能力，其实它不会局限于某一个公司或某一个行业，它具有普适性。”滴滴高级数据科学家高梓尧强调。

![SQLFlow 和滴滴数据的整合逻辑](https://cdn.nlark.com/yuque/0/2019/png/226702/1569746554891-606e4d7c-bc38-4213-8479-6284470708dd.png)

SQLFlow 和滴滴数据的整合逻辑

比如分类预测模型，适用于做产品增长的场景，对特定人群进行定向推荐。而无监督聚类模型，也就是模式识别，在滴滴的产品的应用非常广，比如会根据司机出车时长分布，去整合归纳司机出车的偏好，更好地为司机提供调度建议，进而帮助缓解出行供需。

滴滴首席数据科学家谢梁认为在共建 SQLFlow 过程中，充分体现了算法和数据科学在对数据的理解和应用上的两个不同，以及双方优势互补形成 1+1 大于 2 的合力效果。因为对于传统的算法来讲主要强调对于预测一个给定事件的预测精准性。但是数据科学在预测精准性之上，还强调预测的可解释性。实际上在更广泛的商业层面上，比如运营、营销等更需要了解为什么会这这样发生，这对于业务战略制定、营销方案的确定，以及整个产品序列的设计都有非常大的帮助。

滴滴数据科学团队在过去不到两个月的共建工作中显著扩大了 SQLFlow 的应用场景。根据蚂蚁金服 SQLFlow 项目的产品负责人刘勇峰介绍，滴滴的同事们建议并且参与研发了 SQLFlow 对接 XGBoost 的功能，从而在深度学习模型之外支持树模型；以及对接 unsupervised learning 的能力，支持聚类分析。此外，SQLFlow 基于 SHAP 支持了深度学习模型和树模型的图示化解释。SQLFlow 也支持了滴滴常用的 Hive 数据库系统。

![基于 XGBoost 的汽车价格预测模型（数据来自 Kaggle）的 SHAP 解释图](https://cdn.nlark.com/yuque/0/2019/png/226702/1569746579040-0c76218f-d4a1-4e50-ad94-ca8d781e899e.png)

基于 XGBoost 的汽车价格预测模型（数据来自 Kaggle）的 SHAP 解释图（注：SHAP 值表征了每个特征对模型输出的影响，如图中，较小的 engine_hp“引擎马力”值会降低汽车的预测价格）

“我们是希望通过 SQLFlow 真正能够把数据驱动业务、科学决策的思想，能够在中国传播得更好更远，也希望就是能够通过我们自己的努力，真正让 AI 模型能力大众化和普及化，然后使得我们整个国内的数据分析的科学性、合理性和洞察性，能够逐步提升，甚至达到国际领先。”高梓尧说。

而所有参与项目的同事们对 SQLFlow 的未来都有更大的期待，这是对于开源社区作为一种高效率的工作模式的信任。

### 打造一个 SQL 花园生态

在强调数据驱动的滴滴其实一直积极参与到开源建设中，截至目前，滴滴和蚂蚁金服分别开源了数十个项目。SQLFlow 是双方开源共建的首秀。

对于双方仅一个多月的时间就能够共建三个高价值的模型，谢梁认为很重要的原因是 SQLFlow 已经给滴滴搭建好了底层能力，滴滴相当于做了一个交通领域的几个核心插件，并且通过滴滴插件能力，对整个 SQLFlow 覆盖面和深度方面的底层能力进行了验证和提升，“那么再把这个基础打好之后，我们就相当于造了一个大的花园，我们把土都铺好了，需要什么营养的土，要种什么类型的花，都给他做好了，之后就需要有更多的农民伯伯一起来种田，他们要去种向日葵，我们毕竟精力有限可能就是以种小麦和种主粮为主，更多的经济作物就需要其他开源社区的同学一起来贡献。”

在整个 SQLFlow 开源社区建设方面双方都有更大的愿景，滴滴的分析团队总结的很多模型在 BI 领域具备普适性，而 SQLFlow 在蚂蚁的场景使用模型在金融领域颇有普适性，未来要让更多的人去用上普适的 AI 能力，在 SQLFlow 社区之上会形成一个开源货架式的交易市场，更多懂业务的人把更多商业场景抽象成模型打造成模型库，模型库是 SQLFlow 生态中的重要一环，双方正在讨论如何共建。“你就像走进一个超市，里面有 10万个 SQL，每一个 SQL 就是一个实现了你商业逻辑的模型，你就拿来用就行了，这是终极的一个目标”，谢梁兴奋地谈到。

当然现在的 SQLFlow 还是一个非常年轻的开源项目，需要更多的呵护。虽然目前在开源合作方面中国相比美国还有不少差距，但正是因为越来越多的公司和个人去投身其中为之贡献，差距正在缩小。实际上，几乎所有的 SQLFlow 项目成员都是利用业余时间参与到开源项目中。比如滴滴资深算法工程师陈祥，他平时负责数据治理和应用方向上数据、应用与算法的结合和落地, 在 8 月初听到 SQLFlow 项目就决定参与进来，未来他也会号召很多的人参与到开源建设中。

“开源社区所说的构建大生态，其实大生态还包含着另外一层，就是大家互相学习，然后行业内的所有从业人员进行知识交流。所以当各行各业的同学都在里面贡献自己的经验、技能时，我们其实也能从其他的同学那学习到很多处理数据，或者解决实际问题的方法。”高梓尧所言恰如其分地诠释了开源社区众人拾柴火焰高的魅力。

Gartner 预测“到 2020 年，AI 技术将普遍出现在几乎每一个新的软件产品和服务中。”这其中有蚂蚁金服与滴滴 DS 团队的一份力。

### 项目地址

欢迎感兴趣的同学加入社区讨论：
项目官网：[https://sqlflow.org](https://sqlflow.org)

GitHub地址：[https://github.com/sql-machine-learning/sqlflow](https://github.com/sql-machine-learning/sqlflow)

您也可以使用docker，运行文章中的汽车价格预测模型：**docker run -p 8888:8888 sqlflow/sqlflow:didi**