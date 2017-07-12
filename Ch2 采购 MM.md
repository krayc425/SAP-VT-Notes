# Ch2 采购 MM

## 2.1 采购数据 Procurement

### A. 组织数据

1. Client
2. Company Code（CC）
3. Plant
4. Storage Location（S Loc）/存储地点（共享的）
5. **Purchasing Organization（P Org）** /采购组织（独有的）
6. Purchasing Group/采购组（附加的）

共 6 个 = 3 基本的 + 1 共享的 + 1 独有的 + 1 附加的

#### Storage Location

通过关注物料的 **位置** 和 **状态** ，“面向物流”

在某种意义上，S Loc 就是 ERP 环境下的物料 **“监视器”**

**Combination of plant and storage location must be unique.**

#### Purchasing Organization

Evaluates vendors, negotiates contracts.  
Performs **strategic** activities.  
An enterprise may have more.

##### 三种模式

1. 企业级采购组织，Cross company code  
2. 公司级采购组织，Cross plant  
3. 工厂级采购组织，Plant specific  

#### Purchasing Group

A buyer or group of buyers.  
Performs **operational** activities.  
Not assigned to or related to P Org.（不指派给采购组织，或与采购组织无关）

### B. 主数据

1. Material Master（物料主文件）
2. Vendor Master（供应商主文件）
3. Purchasing Info（采购信息记录）
4. Purchasing Conditions（采购价格策略）

#### Vendor Master

系统只向 **“认证供应商”** 进行采购

#### Purchasing Info

交叉索引数据库，**relates vendors and materials.**  
One info record per combination of vendor and material.  
__供应商提供什么物料？  
物料有什么供应商提供？__

#### Purchasing Conditions

##### Pricing Conditions

* Gross price
* **Discounts** and surcharges
* Freight / shipping

##### Obtained from

* **Purchasing info records**  
* Contracts and agreements  
* Other sources

## 2.2 采购流程

采购业务流程，Based on GBI 2.4  
角色：Customer

| Action | Character | MM | Step | Note |
| :-: | :-: | :-: | :-: | :-: | 
| 创建供应商 | 采购部 | 6 | 1 |
| 创建物料 | 物料部 | 7,8 | 2,3 |
| 采购申请 | 各部门 | 10 | 5 |
| 报价请求 | 采购部 | 12 | 7 |
| 选择供应商 | 采购部 | 13,14 | 8,9 |
| 生成 PO | 采购部 | 16 | 10 |
| 跟踪 PO | 各部门 | 17 | 11 |
| 采购物料入库 | 物料部 | 18 | 12 | 产生**物料凭证** |
| 发票验证 | 财务部 | 20 | 14 | 产生**会计凭证*** |
| 结算应付账款 | 财务部 | 24 | 18 |

*三单（入库单、发票、PO）匹配后，发生所有权的转移、价值的转移，确认应付账款




