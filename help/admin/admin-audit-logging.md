---
description: '在除錯客戶問題時，請使用稽核記錄作為第一個位置。 '
seo-description: '在除錯客戶問題時，請使用稽核記錄作為第一個位置。 '
seo-title: 稽核記錄
title: 稽核記錄
uuid: null
translation-type: tm+mt
source-git-commit: 190ba5c1215782e46c8e544c10679d451fbed134

---


# 稽核記錄 {#audit-logging}

作為 [!UICONTROL  Audit Logging] 除錯客戶問題時的第一個位置。

> [!NOTE]
>
>[!UICONTROL Audit Logging] 目前正在開發中，可能會有所變更。請記錄您在 [!DNL JIRA][!DNL UI] (團隊)中遇到的任何問題

![稽核記錄檢視](assets/audit-logging-img.png)

在 **「稽核類型** 」下拉式選擇器中，選擇下列項目：

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

**物件ID** 是您正在研究的項目的ID。請參閱下列表格，以瞭解哪個ID對應至每個案例中的物件ID：

| 稽核類型 | 物件ID |
---------|----------|
| [!UICONTROL Partner] | 合作夥伴ID- PID |
| [!UICONTROL User] | 使用者 ID |
| [!UICONTROL Group] | B3 |
| [!UICONTROL Datasource Summary] | 資料來源ID |
| [!UICONTROL General Datasource] | 資料來源ID |
| [!UICONTROL Merge Rule Datasource] | 資料來源ID |
| [!UICONTROL Data Feed] | 資料饋送ID |
| [!UICONTROL Data Feed Subscription] | 資料饋送ID |
| [!UICONTROL Trait Summary] | SID(特徵) |
| [!UICONTROL Trait Rule] | SID(特徵) |
| [!UICONTROL Segment Summary] |  |
| [!UICONTROL Destination Summary] |  |
| [!UICONTROL Server-to-Server Destination] | 不適用 |
| [!UICONTROL Derived Signal] | 不適用 |
| [!UICONTROL Model] | 不適用 |
| [!UICONTROL Segment Test Group] | 不適用 |

使用 [!UICONTROL Start Date] ([!DNL UTC])和 [!UICONTROL End Date] ([!DNL UTC])縮小記錄檔的時間間隔。