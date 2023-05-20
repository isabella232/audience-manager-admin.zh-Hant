---
description: 測試環境用於測試Audience Manager實施。 在測試版中所做的更改不會影響生產資料。 Audience Manager測試版環境是生產環境的較小規模的獨立版本。 必須在此環境中輸入和收集要test的所有資料。
seo-description: The beta environment is for testing Audience Manager implementations. Changes made in beta do not affect production data. The Audience Manager beta environment is a smaller-scale, standalone version of the production environment. All the data that you want to test must be entered and collected in this environment.
seo-title: Beta Environment
solution: Audience Manager
title: 測試版環境
uuid: 6a253f4e-96e7-4395-a783-a8eb213b7daf
exl-id: 78d5a1ff-c016-4366-ba34-9814a0d92067
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 3%

---

# 測試版環境 {#beta-environment}

測試環境用於測試Audience Manager實施。 在測試版中所做的更改不會影響生產資料。 Audience Manager測試版環境是生產環境的較小規模的獨立版本。 必須在此環境中輸入和收集要test的所有資料。

## 概述 {#overview}

<!-- beta_environment_admin.xml -->

| 服務 | URL/主機名 | 設定步驟 |
|--- |--- |--- |
| S3 |  | 請參閱 [設定AmazonS3時段](admin-beta-environment.md#provision-s3-buckets)。 |
| DCS | https&amp;colon;//dcs-beta.demdex.net/... | 我們不需要額外的步驟。 請參閱 [在Beta環境中訪問DCS](admin-beta-environment.md#access-dcs-beta-environment)。 |
| UI | https&amp;colon;//bank-beta.demdex | 資料每月從生產環境複製到測試環境。 生產憑據對Beta有效。 |
| API | https&amp;colon;//api-beta.demdex.com/... | 資料每月從生產環境複製到測試環境。 生產憑據對Beta有效。 |

## 設定AmazonS3時段 {#provision-s3-buckets}

>[!NOTE]
>
>我們正在遠離使用 [!DNL FTP/SFTP]。 另外，請注意，出站資料傳輸對測試環境不起作用。

至設定 [!DNL S3] 入站資料的儲存桶：

1. 使用 [**SKMS請求TechOps幫助**](https://skms.adobe.com/) 的子菜單。
1. 轉到 **[!UICONTROL Request TechOps Help]** 的下界。
1. 在 **[!UICONTROL Request Search]**，在搜索欄位中鍵入Audience Manager。
1. 在搜索結果中向下滾動，然後按一下 **Audience Manager- S3入站/出站帳戶設定**。
1. 填寫預配窗口中的欄位並指定 **沙盒環境** 的 **[!UICONTROL Environment]** 的子菜單。

>[!NOTE]
>
>我們勸阻 [!DNL FTP/SFTP] 鼓勵使用 [!UICONTROL Amazon S3]。 我們鼓勵使用 [!UICONTROL Amazon S3] 列於 [AmazonS3：關於](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html)。

## 在Beta環境中訪問DCS {#access-dcs-beta-environment}

訪問 [!UICONTROL DCS] 在beta環境中：

1. 製作 [!UICONTROL DCS] 呼叫，使用 [!DNL curl] [命令](https://curl.haxx.se/docs/manpage.html)。 [!DNL Curl] 是使用許多受支援的協定之一將資料從伺服器傳輸或傳輸到伺服器的工具。

   例如︰`curl -v https://dcs-beta.demdex.net/event`

1. 驗證您的請求是否由測試版提供 [!UICONTROL DCS] 通過查找「[!DNL sandbox]的 [!UICONTROL DCS] 響應標頭。

   例如：

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
