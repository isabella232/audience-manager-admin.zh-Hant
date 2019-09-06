---
description: 測試環境是用於測試Audience Manager實作。在測試版中所做的變更不會影響生產資料。Audience Manager beta版環境是小型獨立版本的生產環境。您要測試的所有資料都必須在此環境中輸入並收集。
seo-description: 測試環境是用於測試Audience Manager實作。在測試版中所做的變更不會影響生產資料。Audience Manager beta版環境是小型獨立版本的生產環境。您要測試的所有資料都必須在此環境中輸入並收集。
seo-title: 測試版環境
solution: Audience Manager
title: 測試版環境
uuid: 6a253f4e-96e7-4395-a783-a8 eb213 b7 df
translation-type: tm+mt
source-git-commit: 7765dbf79c2fb6ca8c4b52fe8090c1fd11f9db27

---


# 測試版環境 {#beta-environment}

測試環境是用於測試Audience Manager實作。在測試版中所做的變更不會影響生產資料。Audience Manager beta版環境是小型獨立版本的生產環境。您要測試的所有資料都必須在此環境中輸入並收集。

## 概述 {#overview}

<!-- beta_environment_admin.xml -->

| 服務 | URL/主機名稱 | 布建步驟 |
|--- |--- |--- |
| S3 |  | 請參閱 [布建Amazon S Buckets](admin-beta-environment.md#provision-s3-buckets)。 |
| DCS | https&amp; amp；冒號；/dcs-beta.demdex.net/.。 | 我們不需要額外的步驟。請參閱 [「測試版環境](admin-beta-environment.md#access-dcs-beta-environment)中的DCS」。 |
| UI | https&amp; amp；冒號；//bank-beta.demdex.com | 資料會從生產環境複製到測試版環境。生產憑證適用於測試版。 |
| API | https&amp; amp；冒號；/api-beta.demdex.com/.。 | 資料會從生產環境複製到測試版環境。生產憑證適用於測試版。 |

## 布建Amazon S Buckets {#provision-s3-buckets}

>[!NOTE]
>
>我們正逐漸脫離使用 [!DNL FTP/SFTP]。此外，請注意，傳出資料傳輸不適用於測試版環境。

若要布 [!DNL S3] 建傳入資料的區間：

1. 使用 [**SKMS請求TechOps說明**](https://skms.adobe.com/) 功能。
1. 前往 **[!UICONTROL Request TechOps Help]** 左側導覽邊欄。
1. In **[!UICONTROL Request Search]**，type in the Audience Manager in the search field.
1. 向下捲動搜尋結果，然後按一下 **「Audience Manager- S傳入/傳出帳戶布建**」。
1. 填寫布建設視窗中的欄位，並在欄位中指定 **沙盒環境****[!UICONTROL Environment]** 。

>[!NOTE]
>
>我們鼓勵使用 [!DNL FTP/SFTP] 並鼓勵 [!UICONTROL Amazon S3]使用。我們鼓勵使用的理由 [!UICONTROL Amazon S3] 列於 [Amazon S3：](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html)關於。

## 在Beta環境中存取DCS {#access-dcs-beta-environment}

若要存取 [!UICONTROL DCS] beta版環境：

1. 使用命令進行 [!UICONTROL DCS][!DNL curl][呼叫](https://curl.haxx.se/docs/manpage.html)。[!DNL Curl] is a tool to transfer data from or to a server，using manually of multied protepents.

   例如︰`curl -v https://dcs-beta.demdex.net/event`

1. 在回應標題中確認您 [!UICONTROL DCS] 的請求是由測試版[!DNL sandbox][!UICONTROL DCS] 提供的。

   例如:

   ```
   curl -v http://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```

<!--
1. Determine the load balancer's endpoint IP addresses.

   Run the `dig` [command](https://en.wikipedia.org/wiki/Dig_(command)) to determine the IP address of the nearest load balancer. The `dig` command queries the Domain Name System and returns the name and IP addresses of the Audience Manager [!UICONTROL Data Collection Servers (DCS)].

   ```
   dig dcs-beta.demdex.net
   ...
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.87.15.51
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 50.16.150.8
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.2.228.100
   ```

1. Using one of the addresses in the above table, add a static DNS entry in the [!DNL `/etc/hosts`] file.

   On Windows, modify [!DNL `c:\WINDOWS\system32\drivers\etc\hosts`].

   For example:

[!DNL `52.87.15.51 samplepartner.demdex.net`]

   >[!NOTE]
   >
   >The addresses change occasionally, so you must keep your [!DNL /etc/hosts] file up to date.

   Additionally, if you need to set up ID synchronization, you must add a similar entry for [!DNL dpm.demdex.net.]

[!DNL `52.87.15.51 dpm.demdex.net`] [!DNL]. 

1. Make a [!UICONTROL DCS] call, using the `curl` [command](https://curl.haxx.se/docs/manpage.html). Curl is a tool to transfer data from or to a server, using one of many supported protocols.

   For example:

[!DNL `https://<domain>/event?product=camera`] 

1. Verify that your request was served by the beta [!UICONTROL DCS] by looking for "sandbox" in the [!UICONTROL DCS] response header.

   For example:

   ```
   curl -v https://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```
-->