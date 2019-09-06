---
description: 使用Audience Manager管理工具中的「公司」頁面建立新公司。
seo-description: 使用Audience Manager管理工具中的「公司」頁面建立新公司。
seo-title: 建立公司簡介
title: 建立公司簡介
uuid: 55de18f8-883d-43Fe-b37 f-e8805 bb92 f
translation-type: tm+mt
source-git-commit: 71bf4cec222428686c1eab0998f66887db06da68

---


# 建立公司簡介 {#create-a-company-profile}

使用Audience Manager管理工具中的 [!UICONTROL Companies] 頁面建立新公司。

<!-- t_create_company.xml -->

>[!NOTE]
>
>您必須擁有該 **[!UICONTROL DEXADMIN]** 角色才能建立新公司。

1. Click **[!UICONTROL Companies]** &gt; **[!UICONTROL Add Company]**.
1. 填寫欄位: 

   * **[!UICONTROL Name]**：(必要)指定公司的名稱。
   * **[!UICONTROL Description]**：(必要)提供公司的描述性資訊，例如產業或其完整名稱。
   * **[!UICONTROL Subdomain]**：(必要)指定公司的子網域。您輸入的文字會顯示為事件呼叫的子網域。這無法變更。它必須是有效 [!DNL URL]字元字串。

      例如，如果您的公司命名 [!DNL AcmeCorp]，則子網域會是 [!DNL acmecorp]。

      Audience Manager會使用 [!UICONTROL Data Collection Server]([!UICONTROL DCS])的子網域。在之前的範例中，如果您的公司完全 [!DNL URL] 處於其中 [!UICONTROL DCS][!DNL acmecorp.demdex.net]。

   * **[!UICONTROL Lifecyle]**：指定公司所要的階段：
      * **[!UICONTROL Active]**：指定該公司將是作用中的Audience Manager用戶端。[!UICONTROL Active] 帳戶是指付費客戶，不僅是諮詢，而是適用於Audience Manager SKU。
      * **[!UICONTROL Demo]**：指定該公司僅供示範用途。報告資料將會自動堆疊。
      * **[!UICONTROL Prospect]**：指定該公司為潛在的Audience Manager客戶，例如提供免費 [!DNL POC] 或帳戶設定的公司展示。
      * **[!UICONTROL Test]**：指定該公司僅供內部測試用途使用。
   * **[!UICONTROL Account Types]**：指定此公司的完整帳戶類型集。沒有帳戶類型與任何其他類型互斥。
      * **[!UICONTROL Full AAM]**：指定該公司將擁有完整的Adobe Audience Manager帳戶，且使用者將擁有登入存取權。
      * **[!UICONTROL MMP]**：指定公司已啓用( [!UICONTROL Master Marketing Profile][!UICONTROL MMP])功能。可 [!UICONTROL MMP] 讓您使用指派給每位訪客然後Audience Manager使用的 [!UICONTROL Experience Cloud ID] ([!DNL MCID])指派給Experience Cloud的觀眾。如果您選取此帳戶類型，也會 [!UICONTROL Experience Cloud ID Service] 自動選取此帳戶類型。

         如需詳細資訊，請參閱 [觀眾服務-主行銷設定檔](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html)。
   * **[!UICONTROL Data Source]**：指定該公司是Audience Manager內的第三方資料供應商。
   * **[!UICONTROL Targeting Partner]**：指定該公司作為Audience Manager客戶的定位平台。
   * **[!UICONTROL Visitor ID Service]**：指定該公司已啓用 [!UICONTROL Experience Cloud Visitor ID Service]使用。

      這可 [!UICONTROL Experience Cloud Visitor ID Service] 在Experience Cloud解決方案中提供通用訪客ID。For more information, see the [Experience Cloud Visitor ID Service user guide](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-overview.html).

   * **[!UICONTROL Agency]**：指定該公司將擁有 [!UICONTROL Agency] 帳戶。



1. Click **[!UICONTROL Create]**. 繼續 [編輯公司描述檔](../companies/admin-manage-company-profiles.md#edit-company-profile)中的指示。

   ![步驟結果](assets/add_company.png)

## 編輯公司描述檔 {#edit-company-profile}

編輯公司的描述檔，包括其名稱、說明、子網域、生命週期等。

<!-- t_edit_company_profile.xml -->

1. 按一下 **[!UICONTROL Companies]**，然後找出並按一下所需的公司以顯示其 [!UICONTROL Profile] 頁面。

   使用 [!UICONTROL Search] 方塊底部或清單底部的分頁控制項來尋找所需的公司。您可以按一下所要的欄標題，以遞增或遞減順序排序每欄。

   ![步驟結果](assets/profile_company.png)

1. 視需要編輯欄位:

   * **[!UICONTROL Name]**：編輯公司名稱。這是必填欄位。
   * **[!UICONTROL Description]**：編輯公司的說明。這是必填欄位。
   * **[!UICONTROL Subdomain]**：(必要)指定公司的子網域。您輸入的文字會顯示為事件呼叫的子網域。這無法變更。它必須是有效 [!DNL URL]字元字串。

      例如，如果您的公司命名 [!DNL AcmeCorp]，則子網域會是 [!DNL acmecorp]。

      Audience Manager會使用 [!UICONTROL Data Collection Server] ([!UICONTROL DCS])的子網域。在之前的範例中，如果您的公司完全 [!DNL URL] 處於其中 [!UICONTROL DCS][!DNL acmecorp.demdex.net]。

   * **[!UICONTROL imsOrgld]**：([!UICONTROL Identity Management System Organization ID])此ID可讓您連接您的公司與Adobe Experience Cloud。
   * **[!UICONTROL Lifecyle]**：指定公司所要的階段：
      * **[!UICONTROL Active]**：指定該公司將是作用中的Audience Manager用戶端。「活動中」帳戶是指付費客戶，不僅是諮詢，而是適用於Audience Manager SKU。
      * **[!UICONTROL Demo]**：指定該公司僅供示範用途。報告資料將會自動堆疊。
      * **[!UICONTROL Prospect]**：指定該公司為潛在的Audience Manager客戶，例如提供免費 [!DNL POC] 或帳戶設定的公司展示。
      * **[!UICONTROL Test]**：指定該公司僅供內部測試用途使用。
   * **[!UICONTROL Account Types]**：指定此公司的完整帳戶類型集。沒有帳戶類型與任何其他類型互斥。
      * **[!UICONTROL Full AAM]**：指定該公司將擁有完整的Adobe Audience Manager帳戶，且使用者將擁有登入存取權。
      * **[!UICONTROL MMP]**：指定公司已啓用主行銷描述檔([!UICONTROL MMP])功能。

         如果您選取此帳戶類型，也會 **[!UICONTROL Visitor ID Service]** 自動選取此帳戶類型。
如需詳細資訊，請參閱 [觀眾服務-主行銷設定檔](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html)。
   * **[!UICONTROL Data Source]**：指定該公司是Audience Manager內的第三方資料供應商。
   * **[!UICONTROL Targeting Partner]**：指定該公司作為Audience Manager客戶的定位平台。
   * **[!UICONTROL Visitor ID Service]**：指定公司已啓用Experience Cloud訪客ID服務。

      Experience Cloud 訪客 ID 服務提供跨 Experience Cloud 解決方案的通用訪客 ID。For more information, see the [Experience Cloud Visitor ID Service user guide](https://microsite.omniture.com/t2/help/en_US/mcvid/mcvid_service.html).

   * **[!UICONTROL Agency]**：指定該公司將擁有代理帳戶。
   * **[!UICONTROL Features]**: 選擇所要的選項:
      * **[!UICONTROL Password Expiration]**：在此公司內設定所有使用者密碼，以在90天後過期，以提高Audience Manager的安全性。
      * **[!UICONTROL Reporting]**：啓用此公司的Audience Manager報告。
      * **[!UICONTROL Role Based Access Controls]**：啓用此公司的角色存取控制。以角色為基礎的存取控制可讓您建立具有不同存取權限的使用者群組。然後，這些群組內的個別使用者只能存取Audience Manager中的特定功能。


1. Click **[!UICONTROL Submit Updates]**.

## 刪除公司描述檔 {#delete-company-profile}

使用Audience [!UICONTROL Companies] Manager [!UICONTROL Admin] 工具中的頁面刪除現有公司。

<!-- t_delete_company.xml -->

>[!NOTE]
>
>您必須擁有該 [!UICONTROL DEXADMIN] 角色才能刪除現有的公司。

1. 若要刪除現有公司，請按一 **[!UICONTROL Companies]**&#x200B;下。

   ![步驟結果](assets/companies.png)

1. 按一下 ![](assets/icon_delete.png) 所需公司 **[!UICONTROL Actions]** 的欄。
1. Click **[!UICONTROL OK]** to confirm the deletion.
