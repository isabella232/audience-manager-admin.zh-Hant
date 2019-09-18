---
description: '在除錯客戶問題時，請首先使用「稽核記錄」。 '
seo-description: '在除錯客戶問題時，請首先使用「稽核記錄」。 '
seo-title: 審核記錄
title: 審核記錄
uuid: null
translation-type: tm+mt
source-git-commit: 190ba5c1215782e46c8e544c10679d451fbed134

---


# 審核記錄 {#audit-logging}

在除 [!UICONTROL  Audit Logging] 錯客戶問題時，請先使用。

> [!NOTE]
>
>[!UICONTROL Audit Logging] 目前正在開發中，且可能會有所變動。 請記錄您在（團隊）中遇到的 [!DNL JIRA] 任何[!DNL UI] 問題

![審計日誌視圖](assets/audit-logging-img.png)

在「審 **核類型** 」下拉式選取器中，選擇下列選項：

* [!UICONTROL Partner]
* [!UICONTROL User]
* [!UICONTROL Group]
* [!UICONTROL Datasource Summary]
* [!UICONTROL General Datasource]
* [!UICONTROL Merge Rule Datasource]
* [!UICONTROL Data Feed]
* [!UICONTROL Data Feed Subscription]
* [!UICONTROL Trait Summary]
* [!UICONTROL Trait Rule]
* [!UICONTROL Segment Summary]
* [!UICONTROL Destination Summary]
* [!UICONTROL Server to Server Destination]
* [!UICONTROL Derived Signal]
* [!UICONTROL Model]
* [!UICONTROL Segment Test Group]

物 **件ID** 是您所研究項目的ID。 請參閱下表，每種情況下，其ID對應於「物件ID」:

| 審計類型 | 物件ID |
---------|----------|
| [!UICONTROL Partner] | 合作夥伴ID - PID |
| [!UICONTROL User] | 使用者 ID |
| [!UICONTROL Group] | B3 |
| [!UICONTROL Datasource Summary] | 資料來源ID |
| [!UICONTROL General Datasource] | 資料來源ID |
| [!UICONTROL Merge Rule Datasource] | 資料來源ID |
| [!UICONTROL Data Feed] |  資料饋送ID |
| [!UICONTROL Data Feed Subscription] |  資料饋送ID |
| [!UICONTROL Trait Summary] | SID（特徵） |
| [!UICONTROL Trait Rule] | SID（特徵） |
| [!UICONTROL Segment Summary] |  |
| [!UICONTROL Destination Summary] |  |
| [!UICONTROL Server-to-Server Destination] | 不適用 |
| [!UICONTROL Derived Signal] | 不適用 |
| [!UICONTROL Model] | 不適用 |
| [!UICONTROL Segment Test Group] | 不適用 |

使 [!UICONTROL Start Date] 用([!DNL UTC]) [!UICONTROL End Date] 和([!DNL UTC])縮小記錄檔的時間間隔。