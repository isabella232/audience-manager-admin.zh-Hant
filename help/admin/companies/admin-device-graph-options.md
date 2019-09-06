---
description: 參與Adobe Experience Cloud Device Co-op的公司可使用裝置圖表選項。如果客戶也與與Audience Manager整合的第三方裝置圖形提供者建立合約關係，則此區域將顯示該裝置圖形的選項。這些選項位於公司>公司名稱>描述檔>裝置圖表選項。
seo-description: 參與Adobe Experience Cloud Device Co-op的公司可使用裝置圖表選項。如果客戶也與與Audience Manager整合的第三方裝置圖形提供者建立合約關係，則此區域將顯示該裝置圖形的選項。這些選項位於公司>公司名稱>描述檔>裝置圖表選項。
seo-title: 適用於公司的裝置圖表選項
title: 適用於公司的裝置圖表選項
uuid: a8ced843-710c-4a8f-a0 d7-ea89 d010 a5 a5
translation-type: tm+mt
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# 適用於公司的裝置圖表選項 {#device-graph-options-for-companies}

[!UICONTROL Device Graph Options] 可供參與的公司使用 [!DNL Adobe Experience Cloud Device Co-op]。如果客戶也與與Audience Manager整合的第三方裝置圖形提供者建立合約關係，則此區域將顯示該裝置圖形的選項。這些選項位於 [!UICONTROL Companies] &gt;公司名稱&gt; [!UICONTROL Profile] &gt; [!UICONTROL Device Graph Options]。

![](assets/adminUIdataSource.png)

此圖使用第三方裝置圖表選項的一般名稱。在生產中，這些名稱來自裝置圖形提供者，而且可能會有所不同。例如 [!DNL LiveRamp] ，選項通常(但不一定總是)：

* 請先閱讀 "[!DNL LiveRamp]"
* 包含不同的中間名稱
* 結尾為「[!UICONTROL - Household]或」[!UICONTROL -Person]

## 已定義裝置圖表選項 {#device-graph-options-defined}

您在此處選取的裝置圖表選項會顯示 [!UICONTROL Device Options] 或隱藏 [!DNL Audience Manager] 客戶建立時可用的選擇 [!UICONTROL Profile Merge Rule]。

### Co-op裝置圖表 {#co-op-graph}

參與 [Adobe Experience Cloud Device Co-op](https://marketing.adobe.com/resources/help/en_US/mcdc/) 的客戶使用這些選項來建立 [!UICONTROL Profile Merge Rule][具有決定性資料和可能性資料](https://marketing.adobe.com/resources/help/en_US/mcdc/mcdc-links.html)的選項。此 [!DNL Corporate Provisioning Team] 選項會透過後端 [!DNL API] 呼叫啓動並停用此選項。您無法勾選或清除這些方塊 [!DNL Admin UI]。此外， **[!UICONTROL Co-op Device Graph]****[!UICONTROL Company Device Graph]** 和選項互斥。客戶可以要求我們啓用一或另一個，但不能同時啓動。勾選後，這會在設定 **[!UICONTROL Co-op Device Graph]**[!UICONTROL Device Options] 中顯示控制 [!UICONTROL Profile Merge Rule]項。

![](assets/adminUI1.png)

### 公司裝置圖表 {#company-graph}

此選項適用於 [!DNL Analytics] 在其報表套裝中使用 [!UICONTROL People] 量度 [!DNL Analytics] 的客戶。此 [!DNL Corporate Provisioning Team] 選項會透過後端 [!DNL API] 呼叫啓動並停用此選項。您無法勾選或清除這些方塊 [!DNL Admin UI]。此外， **[!UICONTROL Company Device Graph]****[!UICONTROL Co-op Device Graph]** 和選項互斥。客戶可以要求我們啓用一或另一個，但不能同時啓動。勾選時：

* 此裝置圖表使用屬於您正在設定之公司的決定性資料(無可能性資料)。
* [!DNL Audience Manager] 自動建立 [!UICONTROL Data Source]`*`名為合作夥伴名稱`*-Company Device Graph-Person`的名稱。在 [!UICONTROL Data Source] 詳細資訊頁面中 [!DNL Audience Manager] ，客戶可以變更合作夥伴名稱、描述，並將 [資料匯出控制](https://marketing.adobe.com/resources/help/en_US/aam/c_dec.html) 套用至此資料來源。
* [!DNL Audience Manager] 客戶 ** 在區段 [!UICONTROL Device Options] 中看不到新設定 [!UICONTROL Profile Merge Rule]。

### LiverAp裝置圖表(人員或家庭) {#liveramp-device-graph}

這些核取方塊會在合作夥伴 [!DNL Admin UI] 建立 [!UICONTROL Data Source] 並選擇 **[!UICONTROL Use as an Authenticated Profile]** 及/或 **[!UICONTROL Use as a Device Graph]**&#x200B;建立時啓用。這些設定的名稱由第三方裝置圖形提供者決定(例如， [!DNL LiveRamp][!DNL TapAd]等)。勾選後，表示您正在設定的公司將使用這些裝置圖表提供的資料。

![](assets/adminUI2.png)

>[!MORE_贊_ this]
>
>* [定義的設定檔合併規則選項](https://marketing.adobe.com/resources/help/en_US/aam/merge-rule-definitions.html)
>* [資料來源設定和功能表選項](https://marketing.adobe.com/resources/help/en_US/aam/datasource-settings-definitions.html)

