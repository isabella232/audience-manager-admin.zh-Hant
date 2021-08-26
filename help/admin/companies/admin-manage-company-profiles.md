---
description: 使用「Audience Manager管理工具」中的「公司」頁面來建立新公司。
seo-description: Use the Companies page in the Audience Manager Admin tool to create a new company.
seo-title: Create a Company Profile
title: 建立公司設定檔
uuid: 55de18f8-883d-43fe-b37f-e8805bb92f7a
exl-id: 80bb8a89-0207-4645-ac42-e73cd10561de
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 4%

---

# 建立公司設定檔 {#create-a-company-profile}

使用「Audience Manager管理工具」中的[!UICONTROL Companies]頁面來建立新公司。

<!-- t_create_company.xml -->

>[!NOTE]
>
>您必須擁有&#x200B;**[!UICONTROL DEXADMIN]**&#x200B;角色，才能建立新公司。

1. 按一下 **[!UICONTROL Companies]** > **[!UICONTROL Add Company]**.
1. 填寫欄位: 

   * **[!UICONTROL Name]**:（必要）指定公司名稱。
   * **[!UICONTROL Description]**:（必要）提供公司的描述性資訊，例如產業或其全名。
   * **[!UICONTROL Subdomain]**:（必要）指定公司的子網域。您輸入的文字會顯示為事件呼叫的子網域。 無法變更。 它必須是[!DNL URL] — 有效字元的字串。

      例如，如果您的公司名為[!DNL AcmeCorp]，則子網域會是[!DNL acmecorp]。

      Audience Manager使用[!UICONTROL Data Collection Server](DCS)的子網域。 在上一個範例中，如果您公司在[!UICONTROL DCS]中的完整[!DNL URL]將是[!DNL acmecorp.demdex.net]。

   * **[!UICONTROL Lifecyle]**:指定公司的所需階段：
      * **[!UICONTROL Active]**:指定公司將是作用中的Audience Manager用戶端。[!UICONTROL Active]帳戶代表付費客戶，不僅是諮詢，還是Audience ManagerSKU。
      * **[!UICONTROL Demo]**:指定公司僅供示範之用。報告資料會自動偽造。
      * **[!UICONTROL Prospect]**:指定公司是潛在的Audience Manager客戶，例如獲得免費的公司， [!DNL POC] 或為銷售示範設定帳戶。
      * **[!UICONTROL Test]**:指定公司僅供內部測試之用。
   * **[!UICONTROL Account Types]**:指定此公司的完整帳戶類型。任何帳戶類型均與任何其他類型互斥。
      * **[!UICONTROL Full AAM]**:指定公司將擁有完整的Adobe Audience Manager帳戶，且使用者擁有登入存取權。
      * **[!UICONTROL MMP]**:指定公司已啟用( [!UICONTROL Master Marketing Profile] [!UICONTROL MMP])功能。[!UICONTROL MMP]可讓使用指派給每個訪客，然後由Audience Manager使用的[!UICONTROL Experience Cloud ID]([!DNL MCID])，在Experience Cloud間共用對象。 如果選擇此帳戶類型，則也會自動選擇[!UICONTROL Experience Cloud ID Service]。

         如需詳細資訊，請參閱[Experience Cloud對象](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en)。
   * **[!UICONTROL Data Source]**:指定公司是Audience Manager內的第三方資料提供者。
   * **[!UICONTROL Targeting Partner]**:指定公司作為Audience Manager客戶的定位平台。
   * **[!UICONTROL Visitor ID Service]**:指定公司已啟用以使 [!UICONTROL Experience Cloud Visitor ID Service]用。

      [!UICONTROL Experience Cloud Visitor ID Service]提供跨Experience Cloud解決方案的通用訪客ID。 如需詳細資訊，請參閱[Experience Cloud訪客ID服務使用指南](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=en)。

   * **[!UICONTROL Agency]**:指定公司將有帳 [!UICONTROL Agency] 戶。



1. 按一下 **[!UICONTROL Create]**. 繼續[編輯公司設定檔](../companies/admin-manage-company-profiles.md#edit-company-profile)中的指示。

   ![步驟結果](assets/add_company.png)

## 編輯公司設定檔 {#edit-company-profile}

編輯公司的設定檔，包括其名稱、說明、子網域、生命週期等。

<!-- t_edit_company_profile.xml -->

1. 按一下「**[!UICONTROL Companies]**」，然後找出並按一下所需的公司，以顯示其「[!UICONTROL Profile]」頁面。

   使用[!UICONTROL Search]方塊或清單底部的分頁控制項，以尋找所需的公司。 您可以按一下所需欄的標題，以遞增或遞減順序排序每個欄。

   ![步驟結果](assets/profile_company.png)

1. 視需要編輯欄位:

   * **[!UICONTROL Name]**:編輯公司名稱。這是必填欄位。
   * **[!UICONTROL Description]**:編輯公司的說明。這是必填欄位。
   * **[!UICONTROL Subdomain]**:（必要）指定公司的子網域。您輸入的文字會顯示為事件呼叫的子網域。 無法變更。 它必須是[!DNL URL] — 有效字元的字串。

      例如，如果您的公司名為[!DNL AcmeCorp]，則子網域會是[!DNL acmecorp]。

      Audience Manager使用[!UICONTROL Data Collection Server](DCS)的子網域。 在上一個範例中，如果您公司在[!UICONTROL DCS]中的完整[!DNL URL]將是[!DNL acmecorp.demdex.net]。

   * **[!UICONTROL imsOrgld]**:([!UICONTROL Identity Management System Organization ID])此ID可讓您連線公司與Adobe Experience Cloud。
   * **[!UICONTROL Lifecyle]**:指定公司的所需階段：
      * **[!UICONTROL Active]**:指定公司將是作用中的Audience Manager用戶端。「作用中」帳戶是指付費客戶，不僅是諮詢，也是Audience ManagerSKU。
      * **[!UICONTROL Demo]**:指定公司僅供示範之用。報告資料會自動偽造。
      * **[!UICONTROL Prospect]**:指定公司是潛在的Audience Manager客戶，例如獲得免費的公司， [!DNL POC] 或為銷售示範設定帳戶。
      * **[!UICONTROL Test]**:指定公司僅供內部測試之用。
   * **[!UICONTROL Account Types]**:指定此公司的完整帳戶類型。任何帳戶類型均與任何其他類型互斥。
      * **[!UICONTROL Full AAM]**:指定公司將擁有完整的Adobe Audience Manager帳戶，且使用者擁有登入存取權。
      * **[!UICONTROL MMP]**:指定公司已啟用「主行銷描述檔([!UICONTROL MMP])」功能。

         如果選擇此帳戶類型，則也會自動選擇&#x200B;**[!UICONTROL Visitor ID Service]**。
如需詳細資訊，請參閱[Experience Cloud對象](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en)。
   * **[!UICONTROL Data Source]**:指定公司是Audience Manager內的第三方資料提供者。
   * **[!UICONTROL Targeting Partner]**:指定公司作為Audience Manager客戶的定位平台。
   * **[!UICONTROL Visitor ID Service]**:指定公司已啟用「Experience Cloud訪客ID服務」。

      Experience Cloud 訪客 ID 服務提供跨 Experience Cloud 解決方案的通用訪客 ID。如需詳細資訊，請參閱[Experience CloudID服務使用手冊](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en)。

   * **[!UICONTROL Agency]**:指定公司將有代理帳戶。
   * **[!UICONTROL Features]**: 選擇所要的選項:
      * **[!UICONTROL Password Expiration]**:將此公司內的所有使用者密碼設為90天後過期，以提高Audience Manager安全性。
      * **[!UICONTROL Reporting]**:啟用此公司的Audience Manager報告。
      * **[!UICONTROL Role Based Access Controls]**:為此公司啟用基於角色的訪問控制。角色型存取控制可讓您建立具有不同存取權限的使用者群組。 然後，這些群組中的個別使用者只能存取Audience Manager中的特定功能。


1. 按一下 **[!UICONTROL Submit Updates]**.

## 刪除公司設定檔 {#delete-company-profile}

使用Audience Manager[!UICONTROL Admin]工具中的[!UICONTROL Companies]頁面來刪除現有公司。

<!-- t_delete_company.xml -->

>[!NOTE]
>
>您必須擁有[!UICONTROL DEXADMIN]角色，才能刪除現有公司。

1. 若要刪除現有公司，請按一下&#x200B;**[!UICONTROL Companies]**。

   ![步驟結果](assets/companies.png)

1. 按一下所需公司&#x200B;**[!UICONTROL Actions]**&#x200B;欄中的![](assets/icon_delete.png)。
1. 按一下&#x200B;**[!UICONTROL OK]**&#x200B;以確認刪除。
