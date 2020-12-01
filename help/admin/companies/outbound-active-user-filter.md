---
description: 請依照下列指示產生完整的同步檔案，其中僅包含最近使用中的使用者。 您可能想要篩選作用中使用者將相關資料推送至現場定位系統，或限制傳送至DSP的檔案大小。 您不能將此篩選器用於增量同步。
seo-description: 請依照下列指示產生完整的同步檔案，其中僅包含最近使用中的使用者。 您可能想要篩選作用中使用者將相關資料推送至現場定位系統，或限制傳送至DSP的檔案大小。 您不能將此篩選器用於增量同步。
seo-title: 僅依活躍使用者篩選傳出資料
title: 僅依活躍使用者篩選傳出資料
uuid: a2b4a385-eee3-458c-b978-09509cacb397
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 8%

---


# 僅依活躍使用者篩選傳出資料{#filter-outbound-data-by-active-users-only}

請依照下列指示產生完整的同步檔案，其中僅包含最近使用中的使用者。 您可能想要篩選作用中使用者將相關資料推送至現場定位系統，或限制傳送至DSP的檔案大小。 您不能將此篩選器用於增量同步。

>[!NOTE]
>
>訪客不需要在選取的客戶網站或其廣告流量中看到，即可符合「作用中」資格。 任何[!DNL Audience Manager]客戶或合作夥伴都可看到這些項目，以符合「有效」資格。

若要僅依作用中使用者篩選：

1. 按一下 **[!UICONTROL Companies]**.
1. 選擇要使用的公司，然後按一下&#x200B;**[!UICONTROL Destinations]**。
1. 在[!UICONTROL Batch Data]區段中，設定下列選項：

   * **[!UICONTROL Sync Type]**:選擇 **[!UICONTROL Customer]** 或 **[!UICONTROL Platform]**。
   * **[!UICONTROL Sync Type Lookback Period]**:此時間間隔定義資料檔案的範圍。選擇包括&#x200B;**[!UICONTROL 24 hours]**、**[!UICONTROL 7 days]**、**[!UICONTROL 30 days]**。
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Select **[!UICONTROL Never]**. 請記住，此篩選器僅適用於完全同步檔案。
   * **[!UICONTROL Full Sync Scheduled Run]**:這會決定您要接收此檔案的頻率。選擇包括&#x200B;**[!UICONTROL 24 hours]**、**[!UICONTROL 7 days]**、**[!UICONTROL 30 days]**&#x200B;或&#x200B;**[!UICONTROL Never]**（要禁用）。

1. 按一下 **[!UICONTROL Save]**.
