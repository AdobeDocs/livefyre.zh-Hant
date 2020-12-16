---
description: 顯示應用程式內25個最熱門的執行緒，依人氣排序。
seo-description: 顯示應用程式內25個最熱門的執行緒，依人氣排序。
seo-title: 熱線程
solution: Experience Manager
title: 熱線程
uuid: 0011f769-6712-48e9-bb10-a43610fef595
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---


# 熱線程{#hot-threads}

顯示應用程式內25個最熱門的執行緒，依人氣排序。

「作用線程」檢視會顯示應用程式中25個最熱門的線程，依人氣高低排列。 這包括應用程式中的所有內容，包括手動貼文、SocialSync的內容以及串流的內容。

>[!NOTE]
>
>「熱線程」可用於「注釋」，但不可用於「即時部落格」或「聊天」。

有關啟用「熱線程」視圖的詳細資訊，請參閱Studio >網路設定。

## 預覽{#section_xhh_2dl_wy}

按一下串流頂端的&#x200B;**[!UICONTROL Hot Threads]**，會以預覽最多25個執行緒的應用程式內容，並顯示應用程式最高的「人氣分數」。 使用Livefyre的專屬演算法和演變演算法，計算每個執行緒的人氣分數。 預覽會顯示最上層的註解，以及最多5個最受歡迎的回覆，以及這5個回覆中每個回覆的直接父項。

如果串流中沒有具有人氣分數的執行緒，則不會顯示任何評論，且使用者會看到訊息&#x200B;**[!UICONTROL There are not enough threads yet]**&#x200B;和連結至&#x200B;**[!UICONTROL See what’s new]**。

熱線程清單不是即時的，只有在刷新頁面或選擇其他視圖（**[!UICONTROL Newest]**&#x200B;或&#x200B;**[!UICONTROL Oldest]**）時才會更新。 （如果評論被協調，且Bozo已處理或已處理，則會立即從清單中移除。）

## Breakout View {#section_zmf_ddl_wy}

在預覽中，按一下&#x200B;**[!UICONTROL Show entire Thread]**&#x200B;將「熱線程」視圖替換為上下文中線程的分段視圖，包括該線程內的每個回覆。 （分組視圖中不顯示其他線程。） 按一下&#x200B;**[!UICONTROL Hot Threads]**&#x200B;返回「熱線程」視圖。

協調者可以在分類檢視中檢視所有待審內容，而內嵌協調則可供使用。 「按贊」、回覆、編輯和協調動作將會在突破檢視中繼續即時串流。

## 從熱線程視圖{#section_bmv_bdl_wy}發佈

從「熱線程」檢視的頂端註解方塊張貼註解，會將使用者切換回「最新」檢視。

張貼在「作用線程」檢視中的回覆或按贊會顯示在串流中，而不會變更檢視。 排序選項和注釋通告程式在「熱線程」視圖中不可用。

為了最佳化效能，Livefyre最多可快取2分鐘的資料。 最近出現的熱線程可能略有延遲。



使用此功能的應用程式：

* [意見](/help/using/c-about-apps/c-comments/c-comments.md)

