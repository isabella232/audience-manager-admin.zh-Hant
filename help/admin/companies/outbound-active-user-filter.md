---
description: 請遵循下列指示，產生僅包含最近使用之使用者的完整同步檔案。您可能想要篩選作用中的使用者將相關資料推送至站上定位系統，或限制傳送至DSP的檔案大小。您無法使用此篩選器與遞增同步。
seo-description: 請遵循下列指示，產生僅包含最近使用之使用者的完整同步檔案。您可能想要篩選作用中的使用者將相關資料推送至站上定位系統，或限制傳送至DSP的檔案大小。您無法使用此篩選器與遞增同步。
seo-title: 僅依主動使用者篩選傳出資料
title: 僅依主動使用者篩選傳出資料
uuid: a2b4a385-eee3-458c-b978-09509cacb397
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# 僅依主動使用者篩選傳出資料 {#filter-outbound-data-by-active-users-only}

請遵循下列指示，產生僅包含最近使用之使用者的完整同步檔案。您可能想要篩選作用中的使用者將相關資料推送至站上定位系統，或限制傳送至DSP的檔案大小。您無法使用此篩選器與遞增同步。

>[!NOTE]
>
>訪客不需要在選定的客戶網站上或其廣告流量中看見，才符合「作用中」的條件。[!DNL Audience Manager] 任何客戶或合作夥伴都可以將它們視為「有效」。

僅供主動使用者篩選：

1. Click **[!UICONTROL Companies]**.
1. 選取您要使用並按一下 **[!UICONTROL Destinations]**&#x200B;的公司。
1. 在 [!UICONTROL Batch Data] 區段中，設定下列選項：

   * **[!UICONTROL Sync Type]**：選擇 **[!UICONTROL Customer]** 或 **[!UICONTROL Platform]**。
   * **[!UICONTROL Sync Type Lookback Period]**：此時間間隔定義資料檔案的範圍。選擇包括 **[!UICONTROL 24 hours]**、**[!UICONTROL 7 days]****[!UICONTROL 30 days]**
   * **[!UICONTROL Incremental Sync Scheduled Run]**：選取 **[!UICONTROL Never]**。請記住，此篩選器僅適用於完全同步檔案。
   * **[!UICONTROL Full Sync Scheduled Run]**：這會決定您要接收此檔案的頻率。選擇包括 **[!UICONTROL 24 hours]****[!UICONTROL 7 days]**、 **[!UICONTROL 30 days]**&#x200B;或 **[!UICONTROL Never]** (停用)。

1. Click **[!UICONTROL Save]**.
