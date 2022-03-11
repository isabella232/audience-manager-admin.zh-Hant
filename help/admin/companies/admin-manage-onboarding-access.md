---
description: 為防止意外檔案和資料登入其他合作夥伴或客戶擁有的目標資料源，Audience Manager在合作夥伴ID(PID)和其他合作夥伴擁有的資料源之間添加了映射要求。
title: 管理第二方資料的登機訪問
source-git-commit: 6c88979f876909bc32b5238605cb4a352e327a00
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# 管理對第二方資料的登機訪問 {#manage-onboarding-access-for-second-party-data}

為防止意外檔案和資料登入其他合作夥伴擁有的目標資料源，Audience Manager在合作夥伴ID(PID)和其他合作夥伴擁有的資料源(DPID)之間添加了映射要求。 閱讀中有關PID和DPID的詳細資訊 [Audience ManagerID的索引](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html)。

出於第二方資料共用目的，如果Audience Manager夥伴或客戶希望將檔案插入他們不擁有的目標資料源，則他們需要請求其夥伴ID(PID)和該特定資料源(DPID)之間的映射。 如果缺少映射，則入站資料作業將不處理檔案，且資料不會裝入Audience Manager。

要建立該映射，請向Audience Manager工程團隊提交Jira票證。 查看示例Jira票證 [這裡](https://jira.corp.adobe.com/browse/AAM-60353)。 您不需要請求為任何現有資料共用關係建立映射。
