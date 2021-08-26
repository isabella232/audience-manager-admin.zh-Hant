---
description: 參與Adobe Experience Cloud Device Co-op的公司可使用「裝置圖表選項」。 如果客戶也與已與Audience Manager整合的協力廠商裝置圖表提供者有合約關係，本區段將顯示該裝置圖表的選項。 這些選項位於公司>公司名稱>設定檔>裝置圖表選項。
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

[!UICONTROL Device Graph Options]適用於參與[!DNL Adobe Experience Cloud Device Co-op]的公司。 如果客戶也與已與Audience Manager整合的協力廠商裝置圖表提供者有合約關係，本區段將顯示該裝置圖表的選項。 這些選項位於[!UICONTROL Companies] >公司名稱> [!UICONTROL Profile] > [!UICONTROL Device Graph Options]中。

![](assets/adminUIdataSource.png)

此圖為協力廠商裝置圖表選項使用一般名稱。 在生產環境中，這些名稱來自裝置圖表提供者，可能與此處所示的不同。 例如，[!DNL LiveRamp]選項通常（但不總是）:

* 請先閱讀 &quot;[!DNL LiveRamp]&quot;
* 包含中間名稱（視情況而定）
* 結尾為&quot;[!UICONTROL - Household]&quot;或&quot;[!UICONTROL -Person]&quot;

## 已定義的裝置圖表選項 {#device-graph-options-defined}

您在此處選擇的設備圖表選項顯示或隱藏[!DNL Audience Manager]客戶建立[!UICONTROL Profile Merge Rule]時可用的[!UICONTROL Device Options]選項。

### Co-op裝置圖表 {#co-op-graph}

參與[Adobe Experience Cloud Device Co-op](https://experienceleague.adobe.com/docs/device-co-op/using/about/overview.html?lang=en)的客戶會使用這些選項，以[確定性和可能性資料](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en)建立[!UICONTROL Profile Merge Rule]。 [!DNL Corporate Provisioning Team]會透過後端[!DNL API]呼叫啟用並停用此選項。 您不能選中或清除[!DNL Admin UI]中的這些框。 此外，**[!UICONTROL Co-op Device Graph]**&#x200B;和&#x200B;**[!UICONTROL Company Device Graph]**&#x200B;選項互斥。 客戶可要求我們啟用其中一個或另一個，但不能同時啟用兩者。 若勾選此選項，[!UICONTROL Profile Merge Rule]的[!UICONTROL Device Options]設定中就會顯示&#x200B;**[!UICONTROL Co-op Device Graph]**&#x200B;控制項。

![](assets/adminUI1.png)

### 公司裝置圖表 {#company-graph}

此選項適用於在[!DNL Analytics]報表套裝中使用[!UICONTROL People]量度的[!DNL Analytics]客戶。 [!DNL Corporate Provisioning Team]會透過後端[!DNL API]呼叫啟用並停用此選項。 您不能選中或清除[!DNL Admin UI]中的這些框。 此外，**[!UICONTROL Company Device Graph]**&#x200B;和&#x200B;**[!UICONTROL Co-op Device Graph]**&#x200B;選項互斥。 客戶可要求我們啟用其中一個或另一個，但不能同時啟用兩者。 若勾選：

* 此裝置圖表使用屬於您所設定之公司的決定性資料（無可能性資料）。
* [!DNL Audience Manager] 自動建立名 [!UICONTROL Data Source] 為「合 `*`作夥伴名稱」`*-Company Device Graph-Person`。在[!UICONTROL Data Source]詳細資訊頁面中，[!DNL Audience Manager]客戶可以更改合作夥伴名稱、說明，並將[資料匯出控制項](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en)應用到此資料源。
* [!DNL Audience Manager] 客 *戶* 在的區段中看 [!UICONTROL Device Options] 不到新設 [!UICONTROL Profile Merge Rule]定。

### LiveRamp裝置圖表（個人或家庭） {#liveramp-device-graph}

當合作夥伴建立[!UICONTROL Data Source]並選擇&#x200B;**[!UICONTROL Use as an Authenticated Profile]**&#x200B;和/或&#x200B;**[!UICONTROL Use as a Device Graph]**&#x200B;時，在[!DNL Admin UI]中啟用這些複選框。 這些設定的名稱由第三方裝置圖表提供者決定（例如[!DNL LiveRamp]、[!DNL TapAd]等）。 若勾選此選項，表示您所設定的公司將使用這些裝置圖表提供的資料。

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [定義的設定檔合併規則選項](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/merge-rule-definitions.html?lang=en)
>* [資料來源設定和功能表選項](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html?lang=en)

