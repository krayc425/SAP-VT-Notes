# Ch3 销售 SD

## 3.1 销售数据

### A. 组织数据

1. Client
2. Company Code（CC）
3. **Sales Area**（独有的），由以下 3 项唯一确定：  
    * Sales Organization / 销售组织
    * Distribution Channel / 销售渠道
    * Division / 产品系列
4. Plant（提供产品和服务，Delivering Plant）
5. Storage Location（共享的）
6. Shipping Point / 发货点（附加的）

共 6 个 = 3 基本的 + 1 独有的 + 1 共享的 + 1 附加的

#### Sales Area

A sales area is uniquely identified by / A sales area is a combination of

* Sales Organization
* Distribution Channel
* Division（Product Family / Product Group）

**A sales area can belong to only a CC**

##### Sales Organization

* Negotiating sales conditions
* Distributing goods and services

##### Distribution Channel

划分客户群

* Wholesale
* Retail
* Internet

##### Division

* Used to represent a product line

#### Plant（Delivering）

Used to deliver product and service

* Manufacturing facility
* Warehouse

#### Shipping Point

A physical location from which **outbound deliveries** are sent

* Loading dock
* Mail room

### B. 主数据

1. Material Master（物料主文件）
2. Customer Master（客户主文件）
3. Sales Info（销售信息记录）
4. Sales Conditions（销售价格策略）

**和采购是对称的**

#### Customer Master

* 销售记录
* 付款信用记录，销售限额
* 交货地，发票寄往地

#### Sales Info

Intersection data for **customer and material**

__客户买过什么物料？
物料被哪些客户买过？__

#### Sales Conditions

* Prices
    * Material Price
    * Customer specific price
* Freight
    * InCoTerms
* Surcharges and discounts
    * For customer, material or combination
* Taxes

## 3.2 销售流程

销售业务流程，Based on GBI 2.4
角色：Vendor

| Action | Section | SD | Step | Note |
| :-: | :-: | :-: | :-: | :-: | 
| 创建客户 |  | 9 | 1 | 
| 创建寻价请求 |  | 12 | 4 | Inquiry |
| **创建报价** | 销售部 | 13 | 5 | Quotation |
| 销售订单 | 销售部 | 14 | 6 | 要输入 PO Num（对方的采购订单号）|
| 可获得性检查 | 物料部 |  |  | 现货 ATP / 自制 / 外购 |
| 发货通知 | 销售部 | 17 | 9 |
| 交付计划 | 销售部 |  |  | 见下 |
| 分拣（包装）| 物料部 | 19 | 11 | 物理变化，产生**物料凭证** |
| 销售发货 | 销售部 | 20 | 12 | 逻辑变化，产生**会计凭证** |
| 创建发票 | 财务部 | 22 | 14 |
| 结算应收账款 | 财务部 | 24 | 16 | 价值转移，产生**会计凭证** |

### 交付计划

#### 后序计划

SAP 默认执行

从交付日期开始往前推

Order Date ← 订单完工/可供销售 ← 运输计划 ← 开始装载 ← 发货 ← 要求/计划交付日期

#### 前序计划

从订单日期开始往后推

Order Date → 订单完工/可供销售 → 运输计划 → 开始装载 → 发货 → 要求/计划交付日期

