---
description: 按照以下說明生成一個僅包括最近活動用戶的完整同步檔案。 您可能希望篩選活動用戶以將相關資料推送到現場目標系統或限制發送到的檔案的大DSP小。 不能將此篩選器用於增量同步。
seo-description: Follow these instructions to generate a full synchronization file that includes recently active users only. You may want to filter for active users to push relevant data to an on-site targeting system or to limit the size of the files sent to a DSP. You cannot use this filter with incremental synchronization.
seo-title: Filter Outbound Data by Active Users Only
title: 僅依活躍使用者篩選傳出資料
uuid: a2b4a385-eee3-458c-b978-09509cacb397
exl-id: d501cfd1-64dd-448e-92c5-180c0081d3e5
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 7%

---

# 僅依活躍使用者篩選傳出資料 {#filter-outbound-data-by-active-users-only}

按照以下說明生成一個僅包括最近活動用戶的完整同步檔案。 您可能希望篩選活動用戶以將相關資料推送到現場目標系統或限制發送到的檔案的大DSP小。 不能將此篩選器用於增量同步。

>[!NOTE]
>
>訪問者無需在選定的客戶站點或廣告流量上看到即可被視為「活動」。 任何人都能看到 [!DNL Audience Manager] 客戶或合作夥伴有資格成為「活動」。

要僅按活動用戶篩選：

1. 按一下 **[!UICONTROL Companies]**.
1. 選擇要使用的公司，然後按一下 **[!UICONTROL Destinations]**。
1. 在 [!UICONTROL Batch Data] 的子菜單。

   * **[!UICONTROL Sync Type]**:選擇 **[!UICONTROL Customer]** 或 **[!UICONTROL Platform]**。
   * **[!UICONTROL Sync Type Lookback Period]**:此時間間隔定義資料檔案的範圍。 選擇包括 **[!UICONTROL 24 hours]**。 **[!UICONTROL 7 days]**。 **[!UICONTROL 30 days]**。
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Select **[!UICONTROL Never]**. 請記住，此篩選器僅適用於完全同步檔案。
   * **[!UICONTROL Full Sync Scheduled Run]**:這決定了您要接收此檔案的頻率。 選擇包括 **[!UICONTROL 24 hours]**。 **[!UICONTROL 7 days]**。 **[!UICONTROL 30 days]**&#x200B;或 **[!UICONTROL Never]** （禁用）。

1. 按一下 **[!UICONTROL Save]**.
