---
description: 預設情況下，所有公司都與Adobe Media Optimizer(AMO)同步資料。 在管理員UI中，每個公司容器都有一個管理此進程的資料源。 此資料源是AdobeAMO(ID 411)。 按一下所選公司的容器行（在「容器」頁籤下）以禁用此預設同步，或向AMO同步進程添加和刪除其他資料源。
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

預設情況下，所有公司都將資料與 [!DNL Adobe Media Optimizer] ([!DNL AMO])。 在 [!UICONTROL Admin UI]，每個公司容器都有一個管理此進程的資料源。 此資料源 [!UICONTROL Adobe AMO] ([!UICONTROL ID] 411)。 按一下容器行(位於 [!UICONTROL Containers] 頁籤)，用於選定公司禁用此預設同步，或將其他資料源添加到 [!DNL AMO] 同步進程。

![](assets/id-sync.png)

## ID同步狀態 {#id-sync-status}

下表說明了資料源的同步狀態。

| 狀態 | 說明 |
|------ | -------- |
| 關閉 | 從中刪除所有資料源 [!UICONTROL Selected Data Sources] 用於此容器禁用ID同步的 [!DNL AMO] |
| 開（不考慮ID服務版本） | 資料源與 [!DNL AMO] 無論ID服務版本在以下情況下： <ul><li>資料源顯示在 [!UICONTROL Selected Data Sources] 清單框。</li><li>的 [!DNL AMO] 複選框 *不是* 的下界。</li></ul> |
| 開（不考慮ID服務版本） | 資料源將與 [!DNL AMO] ID服務版本2.0（或更高版本），當： <ul><li>資料源顯示在 [!UICONTROL Selected Data Sources] 清單框。</li><li>的 [!DNL AMO] 複選框 *是* 的下界。</li></ul> |

>[!MORELIKETHIS]
>
>* [管理容器](../companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967)

