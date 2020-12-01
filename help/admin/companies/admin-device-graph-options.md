---
description: 「裝置圖形選項」適用於參與Adobe Experience Cloud Device Co-op的公司。 如果客戶也與與與Audience Manager整合的第三方裝置圖形提供者有合約關係，本節將顯示該裝置圖形的選項。 這些選項位於「公司>公司名稱>描述檔>裝置圖形選項」中。
seo-description: 「裝置圖形選項」適用於參與Adobe Experience Cloud Device Co-op的公司。 如果客戶也與與與Audience Manager整合的第三方裝置圖形提供者有合約關係，本節將顯示該裝置圖形的選項。 這些選項位於「公司>公司名稱>描述檔>裝置圖形選項」中。
seo-title: 適用於公司的裝置圖表選項
title: 適用於公司的裝置圖表選項
uuid: a8ced843-710c-4a8f-a0d7-ea89d010a7a5
translation-type: tm+mt
source-git-commit: 2998dc049971b2fac8c45ca6e3118ea607ae3f92
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 4%

---


# 適用於公司的裝置圖表選項{#device-graph-options-for-companies}

[!UICONTROL Device Graph Options]適用於參與[!DNL Adobe Experience Cloud Device Co-op]的公司。 如果客戶也與與與Audience Manager整合的第三方裝置圖形提供者有合約關係，本節將顯示該裝置圖形的選項。 這些選項位於[!UICONTROL Companies] >公司名稱> [!UICONTROL Profile] > [!UICONTROL Device Graph Options]。

![](assets/adminUIdataSource.png)

此圖為協力廠商裝置圖形選項使用通用名稱。 在生產中，這些名稱來自裝置圖形提供者，可能與此處顯示的名稱不同。 例如，[!DNL LiveRamp]選項通常（但並不總是）:

* 請先閱讀 &quot;[!DNL LiveRamp]&quot;
* 包含中間名稱（視情況而定）
* 結尾為&quot;[!UICONTROL - Household]&quot;或&quot;[!UICONTROL -Person]&quot;

## 已定義的設備圖形選項{#device-graph-options-defined}

您在此處選取的裝置圖形選項會公開或隱藏[!DNL Audience Manager]客戶建立[!UICONTROL Profile Merge Rule]時可用的[!UICONTROL Device Options]選項。

### Co-op Device Graph {#co-op-graph}

參與[Adobe Experience Cloud Device Co-op](https://marketing.adobe.com/resources/help/en_US/mcdc/)的客戶會使用這些選項建立包含[確定性和概率性資料](https://marketing.adobe.com/resources/help/en_US/mcdc/mcdc-links.html)的[!UICONTROL Profile Merge Rule]。 [!DNL Corporate Provisioning Team]會透過後端[!DNL API]呼叫來啟動並停用此選項。 您不能在[!DNL Admin UI]中選中或清除這些框。 此外，**[!UICONTROL Co-op Device Graph]**&#x200B;和&#x200B;**[!UICONTROL Company Device Graph]**&#x200B;選項互斥。 客戶可以要求我們啟動一個或另一個，但不能同時啟動兩者。 勾選後，會顯示[!UICONTROL Device Options]設定中的&#x200B;**[!UICONTROL Co-op Device Graph]**&#x200B;控制項。[!UICONTROL Profile Merge Rule]

![](assets/adminUI1.png)

### 公司設備圖{#company-graph}

此選項適用於[!DNL Analytics]客戶，這些客戶在[!DNL Analytics]報表套裝中使用[!UICONTROL People]度量。 [!DNL Corporate Provisioning Team]會透過後端[!DNL API]呼叫來啟動並停用此選項。 您不能在[!DNL Admin UI]中選中或清除這些框。 此外，**[!UICONTROL Company Device Graph]**&#x200B;和&#x200B;**[!UICONTROL Co-op Device Graph]**&#x200B;選項互斥。 客戶可以要求我們啟動一個或另一個，但不能同時啟動兩者。 勾選時：

* 此裝置圖表使用屬於您所設定公司的確定性資料（無概率資料）。
* [!DNL Audience Manager] 自動建立名 [!UICONTROL Data Source] 為合作 `*`夥伴名稱`*-Company Device Graph-Person`。在[!UICONTROL Data Source]詳細資訊頁面中，[!DNL Audience Manager]客戶可變更合作夥伴名稱、說明，並將[資料匯出控制](https://marketing.adobe.com/resources/help/en_US/aam/c_dec.html)套用至此資料來源。
* [!DNL Audience Manager] 客戶 *在* 區段中不會看到 [!UICONTROL Device Options] 新的設定 [!UICONTROL Profile Merge Rule]。

### LiveRamp裝置圖表（人員或家庭）{#liveramp-device-graph}

當合作夥伴建立[!UICONTROL Data Source]並選擇&#x200B;**[!UICONTROL Use as an Authenticated Profile]**&#x200B;和／或&#x200B;**[!UICONTROL Use as a Device Graph]**&#x200B;時，這些複選框在[!DNL Admin UI]中啟用。 這些設定的名稱由協力廠商裝置圖形提供者（例如[!DNL LiveRamp]、[!DNL TapAd]等）決定。 勾選後，這表示您所設定的公司將使用這些裝置圖表提供的資料。

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [定義的設定檔合併規則選項](https://marketing.adobe.com/resources/help/en_US/aam/merge-rule-definitions.html)
>* [資料來源設定和功能表選項](https://marketing.adobe.com/resources/help/en_US/aam/datasource-settings-definitions.html)

