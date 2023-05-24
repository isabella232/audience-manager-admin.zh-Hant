---
description: 依預設，所有公司都會與Adobe Media Optimizer (AMO)同步資料。 在管理UI中，每個公司容器都有一個管理此程式的資料來源。 此資料來源為AdobeAMO (ID 411)。 按一下所選公司的容器列（在「容器」標籤下），以停用此預設同步處理，或在AMO同步處理流程中新增和移除其他資料來源。
seo-description: By default, all companies sync data with Adobe Media Optimizer (AMO). In the Admin UI, each company container has a data source that manages this process. This data source is Adobe AMO (ID 411). Click a container row (under the Containers tab) for a selected company to disable this default sync or to add and remove other data sources to the AMO sync process.
seo-title: ID Syncing with Media Optimizer
title: 與 Media Optimizer 同步的 ID
uuid: b741dfa7-2947-4288-b214-79eccf18d53a
exl-id: ebd978ef-3825-4a96-94bd-5cdae269cf7c
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 6%

---

# 與 Media Optimizer 同步的 ID {#id-syncing-with-media-optimizer}

依預設，所有公司都會將資料與 [!DNL Adobe Media Optimizer] ([!DNL AMO])。 在 [!UICONTROL Admin UI]，每個公司容器都有管理此程式的資料來源。 此資料來源為 [!UICONTROL Adobe AMO] ([!UICONTROL ID] 411)。 按一下容器列(在 [!UICONTROL Containers] 索引標籤)，以停用此預設同步處理或新增及移除其他資料來源至 [!DNL AMO] 同步處理序。

![](assets/id-sync.png)

## ID同步狀態 {#id-sync-status}

下表說明資料來源的同步狀態。

| 狀態 | 說明 |
|------ | -------- |
| 關閉 | 從移除所有資料來源 [!UICONTROL Selected Data Sources] 供此容器停用與的ID同步 [!DNL AMO] |
| 開啟（不論ID服務版本為何） | 資料來源會與同步 [!DNL AMO] 無論ID服務版本為何，當： <ul><li>資料來源會出現在 [!UICONTROL Selected Data Sources] 清單。</li><li>此 [!DNL AMO] 核取方塊 *不是* 已選取。</li></ul> |
| 開啟（不論ID服務版本為何） | 資料來源將與 [!DNL AMO] 搭配ID服務2.0版（或更新版本）使用： <ul><li>資料來源會出現在 [!UICONTROL Selected Data Sources] 清單。</li><li>此 [!DNL AMO] 核取方塊 *是* 已選取。</li></ul> |

>[!MORELIKETHIS]
>
>* [管理容器](../companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967)

