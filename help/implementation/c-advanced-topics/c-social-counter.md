---
description: 計算組織的社交項目數。
seo-description: 計算組織的社交項目數。
seo-title: 社交計數器
solution: Experience Manager
title: 社交計數器
uuid: fa9aa1a8-6a04-4bc1-9bfe-e42c1250fd48
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 社交計數器{#social-counter}

計算組織的社交項目數。 如需可用端點的完整清單，請參閱Livefyre [API參考](https://api.livefyre.com/docs) 。

Social計數器API會傳回特定系列中一段時間內符合的組織規則計數。

>[!NOTE]
>
>此API僅適用於Twitter主題標籤。

社交計數器API:

* 資源
* 規則類型
* 回應

## 資源 {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **** networkName:您的Livefyre提供的網路名稱。 例如：中 *的實驗*`labs.fyre.co`室。
* **** 查詢：所有網站的url-safe base64編碼雜湊、文章ID、規則類型元組（預先編碼）

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >查詢限制為10個網站、文章ID、規則類型元組。 （上一個範例將包含3個元組。）

* **from** 指 `(optional)` 定圖形的相對或絕對時段；from指定開頭，若省略，則預設為24小時前。
* **funtil** 指定 `(optional)` 圖形的相對或絕對時段；until指定開始時間，若省略，則預設為目前時間（現在）。

### 相對時間

| 縮寫 | 設備 |
|---|---|
| s | 秒 |
| min | 分鐘 |
| h | 小時數 |
| d | 日 |
| w | 週 |
| mon | 30天（月） |
| y | 365天（年） |

範例:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## 絕對時間 {#section_xqr_jgc_11b}

格式：HH:MM_YYYYMMDD

| 縮寫 | 含義 |
|---|---|
| HH | 小時（24小時時鐘格式） |
| MM | 分鐘 |
| YYYY | 4位數年份 |
| MM | 月 |
| DD | 日 |

範例:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=04:00_20130709 
```

## 規則類型 {#section_v53_xqb_11b}

| 值 | 類型 |
|---|---|
| 2 | Twitter |

範例:

若要取得網站和文章ID `123456` 及規則類型 `some-article-id` 的最後一 `2`分鐘計數，例如： `123456:some-article-id;2:`

```
curl -XGET "https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-1min" 
```

範例回應：

```
{ 
    "status": "ok", 
    "code": 200, 
    "data": { 
        "123456": { 
            "some-article-id": { 
                "2": [ 
                    [ 
                        2, 
                        1374770460 
                    ], 
                    [ 
                        4, 
                        1374770470 
                    ], 
                    [ 
                        3, 
                        1374770480 
                    ], 
                    [ 
                        1, 
                        1374770490 
                    ], 
                    [ 
                        0, 
                        1374770500 
                    ], 
                    [ 
                        7, 
                        1374770510 
                    ] 
                ] 
            } 
        } 
    } 
}
```
