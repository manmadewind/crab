## INTRO 整体架构一览
Added by Marvin

* metrics: 计算相关度的具体方法(包括计算准确率、相似度之类的方法)
  ** base.py: 评价推荐系统的效果
  ** classes.py 有关评价方法的主要实现
  ** cross_validation.py 交叉测试的主要实现
  ** metrics.py 各种评价方法
  ** sampling.py 划分样本为训练集和测试集
  ** pairwise.py 计算一些成对的信息（如计算欧氏距离，皮尔斯相关系数等）

* similarities: 计算相似度的一些方法(具体度量user/item距离的方法是由外部传入的，外部指的是metrics)

* models: Model层

* datasets: 数据访问层

* recommenders 推荐主体（上层应用）（主要有kNN和SVD两大类方法）

### 更模块之间主要的相互依赖、调用关系入下
* Level 1: Recommender 依赖于 Similarities和Models
* Level 2: Similarities 依赖于 Metrics


# Crab - A Recommendation Engine library for Python

  Crab is a ﬂexible, fast recommender engine for Python that integrates classic information ﬁltering recom- 
  mendation algorithms in the world of scientiﬁc Python packages (numpy, scipy, matplotlib). The engine aims 
  to provide a rich set of components from which you can construct a customized recommender system from a 
  set of algorithms.

## Usage

  For Usage and Instructions checkout the [Crab Wiki](https://github.com/muricoca/crab/wiki)

## History
  
  The project was started in 2010  by Marcel Caraciolo as a M.S.C related  project, and since then many people interested joined to help in the project.
  It is currently maintained by a team of volunteers, members of the Muriçoca Labs.

## Authors
  
  Marcel Caraciolo (marcel@muricoca.com)

  Bruno Melo (bruno@muricoca.com)
  
  Ricardo Caspirro (ricardo@muricoca.com)
  
  Rodrigo Alves (rodrigo@muricoca.com)

## Bugs, Feedback

  Please submit bugs you might encounter, as well Patches and Features Requests to the [Issues Tracker](https://github.com/muricoca/crab/issues) located at GitHub.

## Contributions

  If you want to submit a patch to this project, it is AWESOME. Follow this guide:
  
  * Fork Crab
  * Make your alterations and commit
  * Create a topic branch - git checkout -b my_branch
  * Push to your branch - git push origin my_branch
  * Create a [Pull Request](http://help.github.com/pull-requests/) from your branch.
  * You just contributed to the Crab project!

## Wiki

Please check our [Wiki](https://github.com/muricoca/crab/wiki "Crab Wiki") wiki, for further information on how to start developing or use Crab in your projects.

## LICENCE (BSD)

Copyright (c) 2011, Muriçoca Labs

All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:
    * Redistributions of source code must retain the above copyright
      notice, this list of conditions and the following disclaimer.
    * Redistributions in binary form must reproduce the above copyright
      notice, this list of conditions and the following disclaimer in the
      documentation and/or other materials provided with the distribution.
    * Neither the name of the Muriçoca Labs nor the
      names of its contributors may be used to endorse or promote products
      derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL MURIÇOCA LABS BE LIABLE FOR ANY
DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND
ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

