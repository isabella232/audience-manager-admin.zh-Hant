---
description: 範例說明如何使用巨集來建立對外的FTP檔案範本。
seo-description: 範例說明如何使用巨集來建立對外的FTP檔案範本。
seo-title: 檔案格式巨集範例
title: 檔案格式巨集範例
uuid: f00d431d-7e43-457a-b633-c79 cbc4 c8 f10
translation-type: tm+mt
source-git-commit: 4c6d1752ff10d2d3d12cab88e823f25f5ef4fcd0

---


# 檔案格式巨集範例 {#file-format-macro-examples}

範例說明如何使用巨集來建立對外的 [!DNL FTP] 檔案範本。

>[!NOTE]
>
>在表格中 **，boldface** 類型會識別每個巨集及其相關輸出。對於格式範例，已新增&lt;&gt;符號，以協助視覺化個別巨集。

## 通用巨集 {#common-macros}

這些巨集可用於任何格式欄位。請參閱 [檔案格式巨集](../formats/file-formats.md) 以取得完整清單和定義。

<table id="table_B5073597219B470298EE614902DACAE8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 巨集 </th> 
   <th colname="col2" class="entry"> 格式與輸出範例 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>DPID </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; Sync_ TYPE&gt;_&lt; ORDER_ ID&gt;_&lt; DPID&gt;_&lt; SYXCH_ MODE&gt;_&lt;時間戳記&gt;. sync </code> </p> <p>輸出： <code>ftp_215_888_ iter_1449756724.sync </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_ DPID </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; Sync_ TYPE&gt;_&lt; ORDER_ ID&gt;_&lt; DPID&gt;_&lt; STORE_ DPID&gt;_&lt; SYSTER_ MODE&gt;_&lt;時間戳記&gt;. sync </code> </p> <p>輸出： <code>ftp_215_888_20915_ iter_1449756724.sync </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ ID </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; Sync_ TYPE&gt;_&lt; ORDER_ ID&gt;_&lt; DPID&gt;_&lt; SYXCH_ MODE&gt;_&lt;時間戳記&gt;. sync </code> </p> <p>輸出： <code>ftp_215_888_ iter_1449756724.sync </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>同步_ MODE </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; Sync_ TYPE&gt;_&lt; ORDER_ ID&gt;_&lt; DPID&gt;_&lt; SYXCH_ MODE&gt;_&lt;時間戳記&gt;. sync </code> </p> <p>輸出： 
     <ul id="ul_F63D7B78AF1246639D6ED85C1621B17C"> 
      <li id="li_4D0D7B4D047345FE861FCBA2BD0408ED">完整： <code>ftp_215_888_ full_144975672424. sync </code> </li> 
      <li id="li_23F4D1F6B2784E599EDA29AA457327E6">漸進式： <code>ftp_215_888_ iter_1449756724.sync </code> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>同步_類型 </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; Sync_ TYPE&gt;_&lt; ORDER_ ID&gt;_&lt; DPID&gt;_&lt; SYXCH_ MODE&gt;_&lt;時間戳記&gt;. sync </code> </p> <p>輸出： 
     <ul id="ul_11B14E740E40474F8302BDB809C428FE"> 
      <li id="li_54A3EAA468B44AC8B2528F855E03D04B">FTP： <code>ftp_215_888_ iter_1449756724.sync </code> </li> 
      <li id="li_93468C56B661463CA7F62B1F5D3A53FF">https： <code>http_215_888_ iter_1449756724.sync </code> </li> 
      <li id="li_8A204C7BEDBC41C096FE953B5F827DEC">S3： <code>s3_215_888_ iter_1449756724.sync </code> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>時間戳記 </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; Sync_ TYPE&gt;_&lt; ORDER_ ID&gt;_&lt; DPID&gt;_&lt; SYXCH_ MODE&gt;_&lt;時間戳記&gt;. sync </code> </p> <p>輸出： <code>ftp_215_888_ iter_1449756724.sync </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 標題欄位巨集 {#header-field-macros}

僅用於標題欄位的巨集。請參閱 [檔案格式巨集](../formats/file-formats.md) 以取得完整清單和定義。

<table id="table_ABC31B3D660D47969E111EBC734D5BBC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 巨集 </th> 
   <th colname="col2" class="entry"> 格式與輸出範例 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>TAB </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; ORDER_ ID&gt;&lt; TAB&gt;&lt; SYXCH_ TYPE&gt; </code> </p> <p>輸出： <code>888full. sync </code> </p> <p>在輸出中，非列印標籤字元會分隔每個元素。 </p> </td>
  </tr>
 </tbody>
</table>

## 資料行巨集 {#data-row-macros}

僅用於標題欄位的巨集。請參閱 [檔案格式巨集](../formats/file-formats.md) 以取得完整清單和定義。

<table id="table_408C6DD2B9D54550B003EAC93562E64F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 巨集 </th> 
   <th colname="col2" class="entry"> 格式與輸出範例 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>DP_ UUID </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; DP_ UUID&gt;&lt; TAB&gt;&lt; DP_ UUID_ LIST；separator= TAB&gt; </code> </p> <p>輸出： <code>123456UUID1UUID2UUID3UUID </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_ UUID_ LIST </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; DP_ UUID&gt;&lt; TAB&gt;&lt; DP_ UUID_ LIST；separator= TAB&gt; </code> </p> <p>輸出： <code>123456UUID1UUID2UUID3UUID </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SERVER_ LIST&amp;&amp; REEMENT_ SERGE_ LIST </code> </p> </td> 
   <td colname="col2"> <p>此範例會建立一種格式，以傳回伺服器至伺服器饋送中移除的區段。 </p> <p> 
     <code>{「adadtiserId」：「&lt; PIDALAS&gt;」、「dataEnterId」：2，「TID」：「&lt; DP_ UUID&gt;」，
「資料」：[&lt; SERGE_ LIST：{seg|&lt; OPEN_ CURLY_ CASTAR&gt;「名稱」：「&lt; seg. alias&gt;&lt; CLOSE_ Curly_ CASC&gt;}；
separator=」，」&gt;&lt; if(SLOME_ LIST&amp;&amp; ENCERDED_ SERGE_ LIST)&gt;&lt; COMA&gt;&lt; endif&gt;
&lt; REDERTED_ SERME_ LIST：{seg|&lt; OPEN_ CURLY_ CASTAR&gt;「名稱」：「&lt; seg. alias&gt;」，
「ttlineMines」：&lt; CLOSE_ CurLY_ CASTALL&gt;}；separator=」，&gt;]} </code>
  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>Segment_ LIST </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; DP_ UUID&gt;&lt; SERGE_ LIST&gt;；separator=」&gt; </code> </p> <p>輸出： <code>123456105955101183101180101179 </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ TICETS </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; PID&gt;&lt; TAB&gt;&lt; UUID&gt;&lt; UUID&gt;&lt; TAB&gt;&lt; DP_ UUID&gt;&lt; TAB&gt;&lt; SET_ TELICES&gt;&lt; TAB&gt;&lt; OPT_ OUT&gt;&lt; TAB&gt;&lt; SECTION_ LIST：{seg|&lt; seg. type&gt;，&lt; seg. alias&gt;，&lt; OUTPUT_ Attribute_ Value&gt;，&lt; seg. ladpdateTime&gt;&amp;}&gt; </code> </p> <p>輸出： <code>11590008800857968836968564574151629750975075000，17t0aj01b120p1，11247114,1,1343114,1,1343250,1,1343250661000 </code> </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p> <code>TAB </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; DP_ UUID&gt;&lt; TAB&gt;&lt; DP_ UUID_ LIST；separator= TAB&gt; </code> </p> <p>輸出： <code>123456UUID1UUID2UUID3UUID </code> </p> <p>在輸出中，非列印標籤字元會分隔每個元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_ LIST </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; PID&gt;&lt; TAB&gt;&lt; DP_ UUID&gt;&lt; TAB&gt;&lt; SET_ TELICES&gt;&lt; TAB&gt;&lt; TARIT_ LIST；分隔符號=|」&gt; </code> </p> <p>輸出： <code>113112345 123|456|789 </code> </p> </td> 
  </tr> 
 </tbody> 
</table>
