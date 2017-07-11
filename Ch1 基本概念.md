# Ch1 基本概念

## 1.1 基本原理

* ERP：企业资源规划

#### ERP 概念 / 定义（三个层次）

* ERP 是一种先进的**管理思想/模式**
    * 涉及实体：咨询公司/德勤
    
    __ERP 管理模式内涵__
            
    * 以市场需求为导向
    * 以计划用控制为主线
    * 面向供应链/面向流程
    
* ERP 是一套网络化**信息系统**
    1. 管理模式的“物化”
    2. 使用 Internet/Intranet 技术
    
    * 涉及实体：用户/实施 ERP 企业
    
* ERP 是一套商业化**软件产品**
    * 涉及实体/供应商：SAP；产品 ECC6
    
#### ERP 实施（过程）

* 选购一套商品化**软件产品**  
* 建立一个网络化的**信息系统**  
* 导入一种先进的**管理模式**  

#### 制造业方程式（基本规律）

任何制造业企业必须回答的五个问题

1. 生产什么？
2. 需要什么？
3. 现有什么？
4. 还缺什么？
5. 要做什么？

#### MRP 原理
```
                预测  需求  合同（销）
                  ↓    ↓    ↓（生产什么？）
                 主生产计划 MPS
（需要什么？）          ↓（还缺什么？）   （现有什么？）
产品信息 ——————→ 物料需求计划 MRP ←—————— 库存信息
                 ↓（要做什么？）↓
        （供）采购计划       加工计划（产）
```

3/2/1 模型

* 3 个输入
* 2 个输出
* 1 个处理

基于 2 个假设

1. 足够的内部生产能力
2. 足够的外部供应能力

## 1.3 数据综述
    
#### SAP/ERP 数据的三个层次及关系

1. Organizational Data（A)
    * 组织数据，有“层次”，相当于“权限”
2. Master Data（B）
    * 主数据，有“归属”，相当于“数据库”
3. Transaction/Process（C)
    * 基本流程

### A. 组织数据

内部供应链各个模块都具有的权限

1. Client 企业代码
2. Company Code 公司代码
3. Plant 工厂代码

#### Client

* **最高的组织层级**
* 代表：企业集团/集团公司
* 由下属公司/分公司构成

#### Company Code / CC

* **独立的计账单位/法律实体（独立的财务核算单位）**
* 生成资产负债表和损益表
* 财务会计的核心要素

#### Plant

* **获得产品和服务的地方**
* 生产计划和生产执行的核心要素
* 只能被指派给一个公司代码（CC）
* 一个公司代码（CC）可以包含多个工厂

### B. 主数据

1. Material Master 物料主文件    
2. Vendor Master 供应商主文件（上游）
3. Customer Master 客户主文件（下游）

#### Material Master

* 数据丰富
* 分门别类
* 各尽其责

一个物料一个数据库
**避免冗余**

#### Vendor Master & Customer Master

三个视图，不同页卡

* 基本视图
* 财务视图
* 业务视图（Vendor 采购，Customer 销售）

## 1.4 项目实施

实施原则：**信息集成**

职能部门 ERP 项目实施的基本内容

1. 数据
    * **培训**
    * 收集
    * **审核**
    * 录入
2. 流程
    * **识别**
    * **整理**
    * 分析
    * 设计
    * **培训**
    
## 5.2 IWM

####  IM 库存管理

**基于数量**

1. Client
2. Company Code
3. Plant
4. Storage Location（SLoc）

#### WM 仓库管理

**基于位置**

1. 存储区域（大类、货区）
2. 存储区域（细目、货架）

#### IM 和 WM 的关系

集成策略

* 1个仓库代码，至少指派给1个（工厂+）存储位置
* 1个仓库代码，可以指派给多个（工厂+）存储位置
* 1个（工厂+）存储位置，只能指派给1个仓库代码
* 不是所有的（工厂+）存储位置，必须指派给仓库代码

#### Goods Movement

1. Goods receipt（GR）
2. Goods issue（GI）
3. Stock transfer 库存移动（物理移动）
4. Transfer posting 库存转账（逻辑移动）

## 6.1 FI 与 CO

#### FI（Financial Accounting）
 
**财务会计**，对外（提供财务报表），过去
  
* G/L：General Ledger
* AR：Accounts Receivable
* AP：Accounts Payable
  
#### CO（Managerial Accounting）

**管理会计**，对内（成本核算），现在和未来

* Profitability Analysis
* Cost Center Accounting
* Product Cost Controlling

#### 关系

#### 统驭科目（Reconciliation Accounts）

记账记在分类账（Sub-ledgers）上
AR、AP 都是统驭科目


