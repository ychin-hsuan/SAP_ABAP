---
title: 113-1 ABAP 介紹

---

# 113-1 ABAP 介紹

:::info
- [SAP GUI download for Mac](https://hackmd.io/@kikiyang/Hy1tqVdxgl)
- [ABAP 介紹](https://hackmd.io/@kikiyang/SkWyFH_xge)
:::

### ERP 介紹
**E**nterprise **R**esource **P**lanning 企業資源規劃

企業資源規劃系統乃是－ **財務會計導向(Accounting-Oriented)** 的資訊系統
將企業用來滿足顧客訂單所需的資源(採購、生產與配銷運籌...)進行有效的整合
與規劃，以擴大整體經營績效、降低成本

### SAP (德國軟體供應商公司)
- 市場佔有率世界之冠
- 有最佳實務
- 技術與顧問服務兼具

### Logistics Process Flow
![image](https://hackmd.io/_uploads/SyLjm8Ogxg.png)
```
包含採購、生產、庫存、以及銷售

還具有財務會計的功能，對於成本利潤等進行分析

ERP 可以讓訂單進行更有效地規劃
```

### SAP S/4 HANA
![image](https://hackmd.io/_uploads/B1gAmUOgle.png)
`Logistics 物流` `Accounting 會計` `Human Resourses 人資` `Cross Application Functions 跨應用程式之功能`
```
SAP S/4HANA(英文全稱SAP Business Suite 4 SAP HANA)，是由德國軟體企業SAP開發的，基於SAP HANA內存資料庫系統的的企業資源管理軟體。是該公司研發的第四代ERP系統。
ABAP連接所有的模組，現有模組功能不足，可以用ABAP跨模組客製化
```

### ABAP
**A**dvanced **B**usiness **A**pplication **P**rogramming
高級業務應用程式語言
- SAP 上發展工具的程式語言
- 處理 Application Program 的開發（報表 Reporting、對話程式 Dialog …）
- 結合SQL語法特性的第四代程式語言
- 程式物件 Program Object
- 事件導向 Event-Orient

```
SQL全稱是 Structured Query Language，翻譯後就是結構化查詢語言，是一種資料庫查詢和程式設計語言，用於存取資料以及查詢、更新和管理關聯式資料庫系統。
程式物件 Program Object：它將物件作為程式的基本單元，將程式和資料封裝其中，以提高軟體的重用性、靈活性和擴充性，物件裡的程式可以存取及經常修改物件相關連的資料。
事件導向 Event-Orient：傳統的程式設計，寫程式者是主導整個程式的流程，使用者只能按照既定的流程來操作。VB的設計觀念是將所有流程都交給使用者來主控，完全由使用者對視窗內所做出的動作或由系統事件來作決定。
當執行應用程式時，該應用程式即進入待命狀態， 當有按下鍵盤或滑鼠時即是觸動一事件，Windows 將此事件相關訊息傳給該應用程式， 該程式會根據送來的訊息做適當的處理。
```

### SAP Three-tier Architecture
![image](https://hackmd.io/_uploads/r1L0EUdexl.png)
上至下：`Presentation Layer 表現層` `Application Layer 應用層` `Database Layer 資料庫層`
```
圖形使用者介面（英語：Graphical User Interface，縮寫：GUI）
Dispatcher 分派器 像是餐廳服務生
根據優先順序分配工作，接著存取DB
若沒有被分配到的，會進入Buffer緩衝等待
```
---

![image](https://hackmd.io/_uploads/Sk0BrIugxg.png)
上至下：`Presentation Server Layer 表現層 Server` `Application Server Layer 應用層 Server` `Database  資料庫`
```
ABAP能夠呼叫公司報表資源
ABAP 的程式存在 Cross-client，不同 Client 有各自的流程、組織、資料
不同子公司可能存在不同流程，透過ABAP可跨公司處理，如表單撰寫，但表單實體仍存於各公司資料庫
```

### ABAP Dictionary (數據字典)
是SAP定義和管理資料的主要工具
可以用來定義系統中的各類資料對象，包括數據類型、數據結構、數據庫表等等


### ABAP Dictionary 的用處
![截圖 2025-05-07 上午11.44.48](https://hackmd.io/_uploads/Bk0NDLdlll.png)
==確保資料格式正確== ==了解資料代表意義== ==整合/處理/分享資訊==


### ABAP基本物件關係
![截圖 2025-05-07 上午11.47.29](https://hackmd.io/_uploads/HkACPL_eex.png)

![截圖 2025-05-07 上午11.49.28](https://hackmd.io/_uploads/H1pLOLdlgl.png)

### 資料型態設定
==Predefined Type==
- 手動設定型態 (Built-in-type)
- 如同一般資料庫
- 缺點：一次性設定
==Reuse==
- 下層參數可提供不同上層使用
- 同個Data Element可被不同Field使用
- 同個Domain可被不同Data Element使用

**e.g.**
![截圖 2025-05-07 上午11.50.29](https://hackmd.io/_uploads/ryM5_Ldxxx.png)

### 關聯式資料庫(RDBMS)：PK vs FK
==PK 主鍵(Primary Key)==
- 用來**唯一識別欄位**，通常位於Table的第一欄。
==FK 外來鍵(Foreign Key)==
- 用來**連結不同資料表**
- 當兩表之間有關聯時，FK用來將其他Table的PK連結在一起。
# 113-1 ABAP 介紹

:::info
- [SAP GUI download for Mac](https://hackmd.io/@kikiyang/Hy1tqVdxgl)
- [ABAP 介紹](https://hackmd.io/@kikiyang/SkWyFH_xge)
:::

### ERP 介紹
**E**nterprise **R**esource **P**lanning 企業資源規劃

企業資源規劃系統乃是－ **財務會計導向(Accounting-Oriented)** 的資訊系統
將企業用來滿足顧客訂單所需的資源(採購、生產與配銷運籌...)進行有效的整合
與規劃，以擴大整體經營績效、降低成本

### SAP (德國軟體供應商公司)
- 市場佔有率世界之冠
- 有最佳實務
- 技術與顧問服務兼具

### Logistics Process Flow
![image](https://hackmd.io/_uploads/SyLjm8Ogxg.png)
```
包含採購、生產、庫存、以及銷售

還具有財務會計的功能，對於成本利潤等進行分析

ERP 可以讓訂單進行更有效地規劃
```

### SAP S/4 HANA
![image](https://hackmd.io/_uploads/B1gAmUOgle.png)
`Logistics 物流` `Accounting 會計` `Human Resourses 人資` `Cross Application Functions 跨應用程式之功能`
```
SAP S/4HANA(英文全稱SAP Business Suite 4 SAP HANA)，是由德國軟體企業SAP開發的，基於SAP HANA內存資料庫系統的的企業資源管理軟體。是該公司研發的第四代ERP系統。
ABAP連接所有的模組，現有模組功能不足，可以用ABAP跨模組客製化
```

### ABAP
**A**dvanced **B**usiness **A**pplication **P**rogramming
高級業務應用程式語言
- SAP 上發展工具的程式語言
- 處理 Application Program 的開發（報表 Reporting、對話程式 Dialog …）
- 結合SQL語法特性的第四代程式語言
- 程式物件 Program Object
- 事件導向 Event-Orient

```
SQL全稱是 Structured Query Language，翻譯後就是結構化查詢語言，是一種資料庫查詢和程式設計語言，用於存取資料以及查詢、更新和管理關聯式資料庫系統。
程式物件 Program Object：它將物件作為程式的基本單元，將程式和資料封裝其中，以提高軟體的重用性、靈活性和擴充性，物件裡的程式可以存取及經常修改物件相關連的資料。
事件導向 Event-Orient：傳統的程式設計，寫程式者是主導整個程式的流程，使用者只能按照既定的流程來操作。VB的設計觀念是將所有流程都交給使用者來主控，完全由使用者對視窗內所做出的動作或由系統事件來作決定。
當執行應用程式時，該應用程式即進入待命狀態， 當有按下鍵盤或滑鼠時即是觸動一事件，Windows 將此事件相關訊息傳給該應用程式， 該程式會根據送來的訊息做適當的處理。
```

### SAP Three-tier Architecture
![image](https://hackmd.io/_uploads/r1L0EUdexl.png)
上至下：`Presentation Layer 表現層` `Application Layer 應用層` `Database Layer 資料庫層`
```
圖形使用者介面（英語：Graphical User Interface，縮寫：GUI）
Dispatcher 分派器 像是餐廳服務生
根據優先順序分配工作，接著存取DB
若沒有被分配到的，會進入Buffer緩衝等待
```
---

![image](https://hackmd.io/_uploads/Sk0BrIugxg.png)
上至下：`Presentation Server Layer 表現層 Server` `Application Server Layer 應用層 Server` `Database  資料庫`
```
ABAP能夠呼叫公司報表資源
ABAP 的程式存在 Cross-client，不同 Client 有各自的流程、組織、資料
不同子公司可能存在不同流程，透過ABAP可跨公司處理，如表單撰寫，但表單實體仍存於各公司資料庫
```

### ABAP Dictionary (數據字典)
是SAP定義和管理資料的主要工具
可以用來定義系統中的各類資料對象，包括數據類型、數據結構、數據庫表等等


### ABAP Dictionary 的用處
![截圖 2025-05-07 上午11.44.48](https://hackmd.io/_uploads/Bk0NDLdlll.png)
==確保資料格式正確== ==了解資料代表意義== ==整合/處理/分享資訊==


### ABAP基本物件關係
![截圖 2025-05-07 上午11.47.29](https://hackmd.io/_uploads/HkACPL_eex.png)

![截圖 2025-05-07 上午11.49.28](https://hackmd.io/_uploads/H1pLOLdlgl.png)

### 資料型態設定
==Predefined Type==
- 手動設定型態 (Built-in-type)
- 如同一般資料庫
- 缺點：一次性設定
==Reuse==
- 下層參數可提供不同上層使用
- 同個Data Element可被不同Field使用
- 同個Domain可被不同Data Element使用

**e.g.**
![截圖 2025-05-07 上午11.50.29](https://hackmd.io/_uploads/ryM5_Ldxxx.png)

### 關聯式資料庫(RDBMS)：PK vs FK
==PK 主鍵(Primary Key)==
- 用來**唯一識別欄位**，通常位於Table的第一欄。
==FK 外來鍵(Foreign Key)==
- 用來**連結不同資料表**
- 當兩表之間有關聯時，FK用來將其他Table的PK連結在一起。
