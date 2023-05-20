---
description: 設備圖形選項可供參與Adobe Experience Cloud設備合作計畫的公司使用。 如果客戶還與與Audience Manager整合的第三方設備圖形提供商有合同關係，則本節將顯示該設備圖形的選項。 這些選項位於「公司」>「公司名稱」>「配置檔案」>「設備圖形選項」中。
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

的 [!UICONTROL Device Graph Options] 可供參與 [!DNL Adobe Experience Cloud Device Co-op]。 如果客戶還與與Audience Manager整合的第三方設備圖形提供商有合同關係，則本節將顯示該設備圖形的選項。 這些選項位於 [!UICONTROL Companies] >公司名稱> [!UICONTROL Profile] > [!UICONTROL Device Graph Options]。

![](assets/adminUIdataSource.png)

此圖使用第三方設備圖形選項的通用名稱。 在生產中，這些名稱來自設備圖形提供器，可能與此處顯示的名稱不同。 例如， [!DNL LiveRamp] 選項通常（但並不總是）:

* 請先閱讀 &quot;[!DNL LiveRamp]&quot;
* 包含中間名稱
* 以&quot;結束[!UICONTROL - Household]&quot;或&quot;[!UICONTROL -Person]&quot;

## 已定義設備圖形選項 {#device-graph-options-defined}

您在此處選擇的設備圖形選項顯示或隱藏 [!UICONTROL Device Options] 可供選擇 [!DNL Audience Manager] 客戶建立 [!UICONTROL Profile Merge Rule]。

### 合作設備圖 {#co-op-graph}

參與 [Adobe Experience Cloud設備合作](https://experienceleague.adobe.com/docs/device-co-op/using/about/overview.html?lang=en) 使用這些選項建立 [!UICONTROL Profile Merge Rule] 與 [確定性和概率性資料](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en)。 的 [!DNL Corporate Provisioning Team] 通過後端激活並停用此選項 [!DNL API] 呼叫。 您不能在 [!DNL Admin UI]。 另外， **[!UICONTROL Co-op Device Graph]** 和 **[!UICONTROL Company Device Graph]** 選項互斥。 客戶可以要求我們激活一個或另一個，但不能同時激活兩個。 選中後，將顯示 **[!UICONTROL Co-op Device Graph]** 控制項 [!UICONTROL Device Options] 設定 [!UICONTROL Profile Merge Rule]。

![](assets/adminUI1.png)

### 公司設備圖 {#company-graph}

此選項用於 [!DNL Analytics] 使用 [!UICONTROL People] 度量 [!DNL Analytics] 報表套件。 的 [!DNL Corporate Provisioning Team] 通過後端激活並停用此選項 [!DNL API] 呼叫。 您不能在 [!DNL Admin UI]。 另外， **[!UICONTROL Company Device Graph]** 和 **[!UICONTROL Co-op Device Graph]** 選項互斥。 客戶可以要求我們激活一個或另一個，但不能同時激活兩個。 選中時：

* 此設備圖形使用屬於您正在配置的公司的確定性資料（無概率資料）。
* [!DNL Audience Manager] 自動建立 [!UICONTROL Data Source] 調用 `*`夥伴名稱`*-Company Device Graph-Person`。 在 [!UICONTROL Data Source] 詳細資訊頁面， [!DNL Audience Manager] 客戶可以更改合作夥伴名稱、說明並應用 [資料導出控制項](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en) 到此資料源。
* [!DNL Audience Manager] 客戶 *不* 查看 [!UICONTROL Device Options] 的 [!UICONTROL Profile Merge Rule]。

### LiveRamp設備圖表（人員或家庭） {#liveramp-device-graph}

這些複選框在 [!DNL Admin UI] 當合作夥伴建立 [!UICONTROL Data Source] 選擇 **[!UICONTROL Use as an Authenticated Profile]** 和/或 **[!UICONTROL Use as a Device Graph]**。 這些設定的名稱由第三方設備圖形提供程式(例如， [!DNL LiveRamp]。 [!DNL TapAd]等)。 選中後，這意味著您所配置的公司將使用這些設備圖形提供的資料。

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [定義的設定檔合併規則選項](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/merge-rule-definitions.html?lang=en)
>* [資料源設定和菜單選項](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html?lang=en)

