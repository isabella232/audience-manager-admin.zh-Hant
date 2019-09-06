---
description: 部分常用HTTP巨集組合的範例。
seo-description: 部分常用HTTP巨集組合的範例。
seo-title: HTTP格式巨集範例
title: HTTP格式巨集範例
uuid: a81a2e2a-de7 e-4b6 a-8771-fcfa0 dc74570
translation-type: tm+mt
source-git-commit: 4c6d1752ff10d2d3d12cab88e823f25f5ef4fcd0

---


# HTTP格式巨集範例 {#http-format-macro-examples}

一些常用 [!DNL HTTP] 巨集組合的範例。

請參閱 [HTTP格式巨集](../formats/web-formats.md) ，以取得巨集清單及其定義。

<table id="table_D5FAC5D056ED49D79FA883197EF8F42E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 巨集範例 </th> 
   <th colname="col2" class="entry"> 輸出格式 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; PID_ ALIAS&gt;|&lt; DP_ UUID&gt;|&lt; TRAITALIAS_ LIST；separator=」，&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_ alias| dp_ uuid| traimate_1，traimate_2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; PID_ ALIAS&gt;|計數：&lt; NUM_ USER&gt;|使用者：[&lt; USER_ LIST：{user|&lt; user. aamuId&gt;：&lt; user. dpuuid&gt;}；separator=」，&gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>「pid_ alias| count：|使用者：[uuid1：dpuuid1，uuid2：dpuuid2]」</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; USER_ Agent&gt;|&lt; IP&gt;|&lt; IMESTAMP&gt;|&lt; ANDUMENT&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>「Firefox|255.255.255.255|1395758143|42341」</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; USER_ LIST：{u|&lt; u. userAgent&gt;|&lt; u. ip&gt;|&lt; u. timestamp&gt;|&lt; u. random&gt;}；separator=」，&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>「Firefox|255.255.255.255|1395758143|42341」</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; DP_ UUID.1&gt; AND&lt; DP_ UUID.2&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>dpuuid AND和dpuuid2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>使用者：[&lt; USER_ LIST：{user|&lt; user. dPuUID.1&gt; AND&lt; user. dpuuids.2&gt;}；separator=」，&gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>使用者：[dpuuid1AND和dpuuid2]</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_ known_ string= loamlipsum&amp; segid=&lt; TARITALIAS_ LIST；distracter=」，」&gt;&amp; test_ dpuuid_1000=&lt; DP_ UUIDS.1000&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_ known_ string= loremlipsum&amp; segid= traimate_1，trat_2&amp; test_ dpuuid_1000= dpuuid_1000</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_ dpuuids=&lt; DP_ UUID。(DPID)&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_ dpuuids= dpuuid2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>「&lt; PID_ ALIAS&gt;|&lt; DP_ UUID&gt;|&lt; TRAITALIAS_ LIST；separator=」，&gt;|&lt; REDERTED_ TRAITALIAS_ LIST；separator=」，&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_ alias| dp_ uuid| traimate_1，traimate_2|特徵_3，特徵_4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>{「Users」：[&lt; USER_ LIST：{user|&lt; OPEN_ STAMP&gt;
「AAM_ UUID」：「&lt; user. aamuId&gt;」，
「DataAssigner_ UUID」：「&lt; user. dpuuid&gt;」，
「區段」：[&lt; user. segments：{seg|&lt; OPEN_ CASCAR&gt;「區段」：「&lt; seg. TritAlias&gt;」&lt; CLOSE_ CANACK&gt;}；separator=」，&gt;]
「已移除_區段」：[&lt; user. removedSegments：{rseg|&lt; OPEN_ CASCAR&gt;「區段」：「&lt; rseg. TritAlias&gt;」&lt; CONNECT_ CANACK&gt;}；separator=」，&gt;]
&lt; CONNECT_ CASTAR&gt;}；separator=」，&gt;]} </code>
  </p> </td> 
   <td colname="col2"> <p> 
     <code>{
「使用者」：[[[
{
「AAM_ UUID」：「uuid1」，
「DataAssigner_ UUID」：「dpuuid1」，
「區段」：[[[
{
「區段」：「alias1」
}
{
「區段」：「alias2」
}
]
「已移除_區段」：[[[
{
「區段」：「alias3」
}
{
「區段」：「alias4」
}
]
}
]
} </code>
  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>{「Users」：[&lt; USER_ LIST：{user|&lt; OPEN_ STAMP&gt;
「AAM_ UUID」：「&lt; user. aamuId&gt;」，
「DataAssigner_ UUID」：「&lt; user. dpuuid&gt;」，
「區段」：[&lt; user. segments：{seg|&lt; OPEN_ CASCAR&gt;「區段」：「&lt; seg. TritAlias&gt;」，「Status」：「&lt; seg. status&gt;」&lt; CLOSE_ CANACK&gt;}；separator=」，&gt;]
&lt; CONNECT_ CASTAR&gt;}；separator=」，&gt;]} </code>
  </p> </td> 
   <td colname="col2"> <p> 
     <code>{
「使用者」：[[[
{
「AAM_ UUID」：「uuid1」，
「DataAssigner_ UUID」：「dpuuid1」，
「區段」：[[[
{
「區段」：「alias1」
「狀態」：「1」
}
{
「區段」：「alias2」
「狀態」：「0」
}
]
}
]
} </code>
  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; PID_ ALIAS&gt;|&lt; DP_ UUID&gt;|&lt;區段：{seg|&lt; seg. TritialAS&gt;}；separator=\，\&gt;|&lt; REDERTED_ SERVER：{seg|&lt; seg. TritialAS&gt;}；separator=\，\&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_ alias| dp_ uuid| traimate_1，traimate_2|特徵_3，特徵_4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; if(user. segments&amp;&amp; user. removedSegments)&gt;&lt; COMA&gt;&lt; endif&gt;</code> </p> </td> 
   <td colname="col2"> <p>如果欄位 <code>區段</code> 和 <code>RemovedSegments</code> 不是空的，請列印逗號。在串連區段和移除區段的清單時，可使用此條件式的POST請求。 </p> </td> 
  </tr> 
 </tbody> 
</table>
