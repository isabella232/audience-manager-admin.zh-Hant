---
description: 請依照下列指示，產生僅包含最近使用中之使用者的完整同步檔案。 您可能想要篩選作用中的使用者，以推送相關資料至網站上的鎖定目標系統，或限制傳送至DSP的檔案大小。 您無法將此篩選器用於增量同步。
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

請依照下列指示，產生僅包含最近使用中之使用者的完整同步檔案。 您可能想要篩選作用中的使用者，以推送相關資料至網站上的鎖定目標系統，或限制傳送至DSP的檔案大小。 您無法將此篩選器用於增量同步。

>[!NOTE]
>
>訪客不需要出現在選取的客戶網站上或其廣告流量中，即可符合「作用中」資格。 任何人都可以看見它們 [!DNL Audience Manager] 符合資格為「作用中」的客戶或合作夥伴。

僅依作用中使用者篩選：

1. 按一下 **[!UICONTROL Companies]**.
1. 選取您要使用的公司，然後按一下 **[!UICONTROL Destinations]**.
1. 在 [!UICONTROL Batch Data] 區段，設定下列選項：

   * **[!UICONTROL Sync Type]**：選取 **[!UICONTROL Customer]** 或 **[!UICONTROL Platform]**.
   * **[!UICONTROL Sync Type Lookback Period]**：此時間間隔會定義資料檔案的範圍。 選項包括 **[!UICONTROL 24 hours]**， **[!UICONTROL 7 days]**， **[!UICONTROL 30 days]**.
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Select **[!UICONTROL Never]**. 請記住，此篩選器僅適用於完整同步檔案。
   * **[!UICONTROL Full Sync Scheduled Run]**：這會決定您接收此檔案的頻率。 選項包括 **[!UICONTROL 24 hours]**， **[!UICONTROL 7 days]**， **[!UICONTROL 30 days]**，或 **[!UICONTROL Never]** （以停用）。

1. 按一下 **[!UICONTROL Save]**.
