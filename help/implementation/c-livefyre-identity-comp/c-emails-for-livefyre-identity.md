---
description: null
seo-description: null
seo-title: Livefyre身分識別的電子郵件
solution: Experience Manager
title: Livefyre身分識別的電子郵件
uuid: 4e807803-687e-4df0-94d1-b18 a48 d48 d8
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Livefyre身分識別的電子郵件{#emails-for-livefyre-identity}

Livefyre Identity會傳送下列電子郵件：

* [密碼重設電子郵件](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [驗證電子郵件](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [傳送使用者電子郵件驗證](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [歡迎電子郵件](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [傳送歡迎電子郵件給使用者](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

您可以自訂所有Livefyre Identity電子郵件的外觀和感覺， **[!UICONTROL Integration Settings > Email Notifications.]**

## 密碼重設電子郵件 {#section_nd1_whs_p1b}

當使用者嘗試重設密碼時，Livefyre會自動傳送密碼重設電子郵件。

密碼重設電子郵件看起來如下：

**主旨：** 重設密碼

**內文：**

請至< *username>*，

我們要求變更您的設定檔在 *<網路名稱>上的密碼*。

如果您要求此項目，請按一下下列連結以選擇新密碼： *< password重設URL>*。

*< Username>*、 *<網路名稱>和**<密碼重設URL>* 均會根據網站訪客和您的網路動態產生。

## 驗證電子郵件 {#section_ak5_xhs_p1b}

您可以傳送電子郵件確認使用者的電子郵件地址。若要傳送驗證電子郵件，您必須開啓 **「整合設定> Livefyre Identity**」中的選項。

驗證電子郵件看起來如下所示：

**主旨：** 電子郵件驗證

**內文：**

< *username>*，

請按一下下列連結(或在您的瀏覽器中貼上)以確認您的帳戶： *<驗證URL>*。

此連結將於24小時後過期。

謝謝您，

< *客戶名稱>* 團隊

*< Username>*、 *<網路名稱>*和 *<驗證URL>* 均會根據網站訪客和您的網路動態產生。

## 傳送電子郵件驗證給使用者 {#section_vyv_yhs_p1b}

您可以傳送電子郵件給使用者，確認他們用來註冊帳戶的電子郵件地址。若要傳送驗證電子郵件：

1. 在Studio中，按一下齒輪圖示以修改網路設定。
1. 按一下 **「整合設定> Livefyre身分識別」。**

1. 導覽至 **「登入類型**」。
1. 按一下 **「需要電子郵件驗證** 」，以傳送電子郵件給驗證客戶用來註冊帳戶的電子郵件地址。
1. 導覽 **至「網路電子郵件」** 以設定電子郵件 **的標誌**、電子郵件地址作為來自地址的電子**郵件**地址，以及用於電子郵件地址的顯示名稱(**電子郵件顯示名稱**)。

## 歡迎電子郵件 {#section_z2v_zhs_p1b}

您可以傳送歡迎電子郵件給使用者。若要傳送歡迎電子郵件，您必須開啓 **「整合設定** > **Livefyre Identity**」中的選項。

歡迎電子郵件看起來如下：

**主旨：** 歡迎使用 *<客戶名稱>*

**內文：**

< *username>*，

為您建立 *了<客戶名稱>的帳戶*。

此帳戶是在 *<反向連結URL>* 從IP位址 *> IP位址>建立*的。

如果您這麼做，可以安全地忽略這封電子郵件。

如果您沒有這麼做，請聯絡 `support@livefyre.com`

謝謝謝謝

「 *客戶名稱」* 團隊

*「UserName」、「customer name」、「referencer URL」* 和「IP位址」全都是根據網站訪客和您的網路動態產生。

## 傳送歡迎電子郵件給使用者 {#section_kjp_c3s_p1b}

您可以在使用者註冊帳戶後，傳送歡迎電子郵件給使用者。如果您設定驗證電子郵件，Studio會傳送驗證電子郵件後傳送此電子郵件。若要傳送歡迎電子郵件：

1. 在Studio中，按一下齒輪圖示以修改網路設定。
1. 按一下 **[!UICONTROL Integration Settings > Livefyre Identity]**

1. 導覽 **[!UICONTROL Email Settings]**至。

1. 按一下 **[!UICONTROL Send Welcome Emails To New Users]** 以啓用電子郵件傳送。
1. 導覽至 **[!UICONTROL Network Email]** 以設定電子郵件 *標誌*、電子郵件地址作為來自地址的電子郵件地址(**電子郵件寄件者**)，以及用於電子郵件地址的顯示名稱(**電子郵件顯示名稱**)。
