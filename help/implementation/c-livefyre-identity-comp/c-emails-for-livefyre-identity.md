---
description: 'null'
seo-description: 'null'
seo-title: Livefyre身分識別電子郵件
solution: Experience Manager
title: Livefyre身分識別電子郵件
uuid: 4e807803-687e-4df0-94d1-b18a48d024e8
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 1%

---


# Livefyre Identity的電子郵件{#emails-for-livefyre-identity}

Livefyre Identity會傳送下列電子郵件：

* [密碼重設電子郵件](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [驗證電子郵件](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [傳送電子郵件驗證給使用者](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [歡迎電子郵件](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [傳送歡迎電子郵件給使用者](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

您可以自訂&#x200B;**[!UICONTROL Integration Settings > Email Notifications.]**&#x200B;中所有Livefyre身分識別電子郵件的外觀和感覺

## 密碼重設電子郵件{#section_nd1_whs_p1b}

當使用者嘗試重設密碼時，Livefyre會自動傳送密碼重設電子郵件。

密碼重設電子郵件的外觀如下：

**主旨：重** 設密碼

**內文:**

*&lt;username>*,

有人要求在&#x200B;*&lt;network name>*&#x200B;中更改配置式的密碼。

如果您要求此密碼，請按一下下列連結以選擇新密碼：*&lt;password reset URL>*。

*&lt;username>*、和 *&lt;network name=&quot;&quot;>*&#x200B;都是 *&lt;password reset=&quot;&quot; URL=&quot;&quot;>* 根據網站訪客和您的網路動態產生的。

## 驗證電子郵件{#section_ak5_xhs_p1b}

您可以傳送電子郵件，驗證使用者的電子郵件地址。 若要傳送驗證電子郵件，您必須開啟&#x200B;**「整合設定> Livefyre Identity」（Livefyre身分識別）中的選項。**

驗證電子郵件的外觀如下：

**主旨：電子** 郵件驗證

**內文:**

您好&#x200B;*&lt;username>*,

請按一下下列連結（或貼在您的瀏覽器中）以驗證您的帳戶：*&lt;verification URL>*。

此連結將於24小時內到期。

謝謝，

*&lt;customer name>*&#x200B;團隊

*&lt;username>*、和 *&lt;network name=&quot;&quot;>*&#x200B;都是 *&lt;verification URL=&quot;&quot;>* 根據網站訪客和您的網路動態產生的。

## 傳送電子郵件驗證給使用者{#section_vyv_yhs_p1b}

您可以傳送電子郵件給使用者，以驗證使用者用來註冊帳戶的電子郵件地址。 若要傳送驗證電子郵件：

1. 在Studio中，按一下齒輪圖示以修改網路設定。
1. 按一下「**整合設定> Livefyre Identity」。**

1. 導覽至&#x200B;**登入類型**。
1. 按一下「要求電子郵件驗證&#x200B;**」，傳送電子郵件給驗證使用者用來註冊帳戶的電子郵件地址的使用者。**
1. 導覽至&#x200B;**網路電子郵件**&#x200B;以設定電子郵件&#x200B;**的**&#x200B;標誌、要用作寄件地址的電子郵件地址（**電子郵件寄件者**），以及用於寄件者電子郵件地址的顯示名稱（**電子郵件顯示名稱**）。

## 歡迎電子郵件 {#section_z2v_zhs_p1b}

您可以傳送歡迎電子郵件給使用者。 若要傳送歡迎電子郵件，您必須開啟「整合設定」>「**>** Livefyre Identity」**中的選項。**

歡迎電子郵件的外觀如下：

**主旨：** 歡迎使用  *&lt;customer name=&quot;&quot;>*

**內文:**

您好&#x200B;*&lt;username>*,

已在&#x200B;*&lt;customer name>*&#x200B;上為您建立帳戶。

此帳戶是在&#x200B;*&lt;轉介URL>*&#x200B;上，從IP位址&#x200B;*&lt;IP位址>*&#x200B;建立。

如果您這麼做，您可以完全忽略此電子郵件。

如果您未執行此動作，請聯絡`support@livefyre.com`

謝謝

*「客戶名稱」*&#x200B;團隊

*「使用者名稱」、「客戶名稱」、「反向連結URL」* 和「IP位址」都會根據網站訪客和您的網路動態產生。

## 傳送歡迎電子郵件給使用者{#section_kjp_c3s_p1b}

在使用者註冊帳戶後，您可以傳送歡迎電子郵件給使用者。 如果您設定驗證電子郵件，Studio會在傳送驗證電子郵件後傳送此電子郵件。 若要傳送歡迎電子郵件：

1. 在Studio中，按一下齒輪圖示以修改網路設定。
1. 按一下 **[!UICONTROL Integration Settings > Livefyre Identity]**

1. 導覽至&#x200B;**[!UICONTROL Email Settings]**。

1. 按一下&#x200B;**[!UICONTROL Send Welcome Emails To New Users]**&#x200B;以啟用傳送電子郵件。
1. 導覽至&#x200B;**[!UICONTROL Network Email]**&#x200B;以設定&#x200B;*電子郵件標誌*、要用作寄件地址的電子郵件地址（**電子郵件寄件者**），以及用於寄件者電子郵件地址的顯示名稱（**電子郵件顯示名稱**）。
