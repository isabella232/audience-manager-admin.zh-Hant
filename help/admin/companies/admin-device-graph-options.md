---
description: 參與Adobe Experience Cloud Device Co-op的公司可使用Device Graph選項。 如果客戶與整合至Audience Manager的第三方裝置圖表提供者也有合約關係，本節將顯示該裝置圖表的選項。 這些選項位於「公司>公司名稱>設定檔>裝置圖表選項」中。
seo-description: The Device Graph Options are available to companies that participate in the Adobe Experience Cloud Device Co-op. If a customer also has a contractual relationship with a third-party device graph provider that is integrated with Audience Manager, this section will show options for that device graph. These options are located in Companies > company name > Profile > Device Graph Options.
seo-title: Device Graph Options for Companies
title: 適用於公司的裝置圖表選項
uuid: a8ced843-710c-4a8f-a0d7-ea89d010a7a5
exl-id: 2502f3d2-b43c-410c-acb6-03c2a2ba2c1d
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 3%

---

# 適用於公司的裝置圖表選項 {#device-graph-options-for-companies}

此 [!UICONTROL Device Graph Options] 可供參與「 」的公司使用 [!DNL Adobe Experience Cloud Device Co-op]. 如果客戶與整合至Audience Manager的第三方裝置圖表提供者也有合約關係，本節將顯示該裝置圖表的選項。 這些選項位於 [!UICONTROL Companies] >公司名稱> [!UICONTROL Profile] > [!UICONTROL Device Graph Options].

![](assets/adminUIdataSource.png)

此圖例使用第三方裝置圖表選項的通用名稱。 在生產環境中，這些名稱會來自裝置圖表提供者，可能會因此處顯示的名稱而異。 例如， [!DNL LiveRamp] 選項通常（但不總是）：

* 請先閱讀 &quot;[!DNL LiveRamp]&quot;
* 包含中間名，名稱會有所不同
* 結尾為&quot;[!UICONTROL - Household]「或」[!UICONTROL -Person]&quot;

## 定義的裝置圖表選項 {#device-graph-options-defined}

您在此選取的裝置圖表選項會公開或隱藏 [!UICONTROL Device Options] 可供選擇的選項 [!DNL Audience Manager] 客戶建立 [!UICONTROL Profile Merge Rule].

### Co-op裝置圖表 {#co-op-graph}

參與「 」的客戶 [Adobe Experience Cloud Device Co-op](https://experienceleague.adobe.com/docs/device-co-op/using/about/overview.html?lang=en) 使用這些選項來建立 [!UICONTROL Profile Merge Rule] 替換為 [確定性資料和概率資料](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en). 此 [!DNL Corporate Provisioning Team] 透過後端啟用和停用此選項 [!DNL API] 呼叫。 您無法核取或清除 [!DNL Admin UI]. 此外， **[!UICONTROL Co-op Device Graph]** 和 **[!UICONTROL Company Device Graph]** 選項互斥。 客戶可以要求我們啟用其中一個，但不能同時啟用兩者。 一旦勾選，系統就會公開 **[!UICONTROL Co-op Device Graph]** 中的控制項 [!UICONTROL Device Options] 設定 [!UICONTROL Profile Merge Rule].

![](assets/adminUI1.png)

### 公司裝置圖表 {#company-graph}

此選項適用於 [!DNL Analytics] 使用 [!UICONTROL People] 量度在其中 [!DNL Analytics] 報告套裝。 此 [!DNL Corporate Provisioning Team] 透過後端啟用和停用此選項 [!DNL API] 呼叫。 您無法核取或清除 [!DNL Admin UI]. 此外， **[!UICONTROL Company Device Graph]** 和 **[!UICONTROL Co-op Device Graph]** 選項互斥。 客戶可以要求我們啟用其中一個，但不能同時啟用兩者。 選取時：

* 此裝置圖表使用屬於您設定之公司的確定性資料（無機率資料）。
* [!DNL Audience Manager] 自動建立 [!UICONTROL Data Source] 已呼叫 `*`合作夥伴名稱`*-Company Device Graph-Person`. 在 [!UICONTROL Data Source] 詳細資訊頁面， [!DNL Audience Manager] 客戶可以變更合作夥伴名稱、說明並套用 [資料匯出控制](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en) 至此資料來源。
* [!DNL Audience Manager] 客戶 *不要* 在中檢視新設定 [!UICONTROL Device Options] 區段 [!UICONTROL Profile Merge Rule].

### LiveRamp裝置圖表（個人或家庭） {#liveramp-device-graph}

這些核取方塊會在 [!DNL Admin UI] 當合作夥伴建立 [!UICONTROL Data Source] 並選取 **[!UICONTROL Use as an Authenticated Profile]** 和/或 **[!UICONTROL Use as a Device Graph]**. 這些設定的名稱由協力廠商裝置圖表提供者決定(例如 [!DNL LiveRamp]， [!DNL TapAd]、等)。 如果勾選，表示您設定的公司將會使用這些裝置圖表提供的資料。

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [定義的設定檔合併規則選項](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/merge-rule-definitions.html?lang=en)
>* [資料來源設定和功能表選項](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html?lang=en)

