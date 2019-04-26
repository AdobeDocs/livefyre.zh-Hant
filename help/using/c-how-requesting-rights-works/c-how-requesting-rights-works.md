---
description: 瞭解權限要求的運作方式。當您將使用者產生的內容(UGC)帶入Livefyre應用程式時，內容會包含可重復使用的權限。您必須擁有作者使用Twitter或Instagram內容的權限。
seo-description: 瞭解權限要求的運作方式。當您將使用者產生的內容(UGC)帶入Livefyre應用程式時，內容會包含可重復使用的權限。您必須擁有作者使用Twitter或Instagram內容的權限。
seo-title: 請求權限
title: 請求權限
uuid: d3194afa-f3 c6-44ed-b03 f-9b1 mark50 c1 d3
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 請求權限{#requesting-rights}

瞭解權限要求的運作方式。當您將使用者產生的內容(UGC)帶入Livefyre應用程式時，內容會包含可重復使用的權限。您必須擁有作者使用Twitter或Instagram內容的權限。

下列權限狀態可從資料庫、應用程式內容、ModQ和AEM Commerce取得：

* **[!UICONTROL Granted]**. 當作者授與您重復使用其內容的權限時，資產的狀態會變更 **[!UICONTROL Granted]**為。

* **[!UICONTROL Expired]**. Livefyre會監視作者的Instagram和Twitter串流，以便回覆14天。在14天後，請求會過期，權限要求狀態會變更為 **[!UICONTROL Expired]**，您可以傳送第二個請求或從書庫中移除該項目。
* **[!UICONTROL Requested]**. 請求來自資料庫的內容權限。您可以一次對一個或多個資產執行此動作。請求權限後，Livefyre會將資產狀態設 **[!UICONTROL Requested]**為。
* **[!UICONTROL Needs Review]**. 如果作者回覆的附註未包含您的# Approval Hashtag，則資產變更狀態 **[!UICONTROL Needs Review]**為。

* **[!UICONTROL Request Failed]**. 無法傳送請求(因為過期的代號等)。
* **[!UICONTROL Request Pending]**. Queues the Rights Request so that that that not toulds at one time.

您可以要求您從Twitter和Instagram取得資產的權利。您必須將資產儲存至「資料庫」以請求權限。

您必須設定 *Instagram商業帳戶* ，使用部分自動化的工作流程，向Instagram索取資產的權利。

您只能將此功能用於由業務帳戶搜尋或串流搜尋所取得的內容。若要申請從個人Instagram帳戶取得的內容權限，您必須手動傳送權限請求。

>[!NOTE]
>
>如需各種Instagram帳戶以及如何使用的詳細資訊，請參閱 [關於Instagram帳戶](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。如需如何申請Instagram帳戶權限的詳細資訊，請參閱 [「傳送手動權限請求](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md#c_send_instagram_manual_rights_request) 及 [傳送部分自動化權限請求](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md#c_send_an_instagram_rights_request_from_the_library)」。

