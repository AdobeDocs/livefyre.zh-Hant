---
description: 計算已策劃的社交項目數目。
seo-description: 計算已策劃的社交項目數目。
seo-title: 社交計數器
solution: Experience Manager
title: 社交計數器
uuid: fa9aa1a8-6a04-4bc1-9bfe-e42 c1250 fd48
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 社交計數器{#social-counter}

計算已策劃的社交項目數目。有關可用端點的完整清單，請參閱「Livefyre [API參考](https://api.livefyre.com/docs) 」區段。

Social計數器API傳回計數，在一段時間內針對特定系列內的相符組織規則傳回計數。

>[!NOTE]
>
>此API僅適用於Twitter主題標籤。

社交計數器API：

* 資源
* 規則類型
* 回應

## 資源 {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **socialName：** 您的Livefyre提供的網路名稱。例如： *實驗室*`labs.fyre.co`。
* **查詢：** 所有網站的url-safe base64編碼雜湊、文章ID、計算資訊應擷取的規則類型片段(預先編碼)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >查詢限於10個網站、文章ID、規則類型元組。(上一個範例會包含個整數)。

* **從**`(optional)` 指定相對或絕對時段至圖形；從指定開始和預設到24小時前(若省略)。
* **直到**`(optional)` 指定相對或絕對時段至圖形；直到已將開始和預設指定為目前時間(現在)(若省略)。

### 相對時間

| 縮寫 | Unit |
|---|---|
| s | 秒數 |
| minimum | 分鐘 |
| h | 小時 |
| d | 日 |
| w | 周數 |
| mon | 30天(月) |
| y | 365天(年) |

範例:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## 絕對時間 {#section_xqr_jgc_11b}

格式：HH：MM_ YYYYMMDD

| 縮寫 | 意謂意義 |
|---|---|
| HH | 小時(以24h時鐘格式) |
| MM | 分鐘 |
| YYYY | 位數年份 |
| MM | 月 |
| DD | Day |

範例:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=04:00_20130709 
```

## 規則類型 {#section_v53_xqb_11b}

| Value | Type |
|---|---|
| 2 | Twitter |

範例:

若要在網站 `123456` 和文章ID `some-article-id` 和規則類型的最後一刻獲得計數 `2`，例如： `123456:some-article-id;2:`

```
curl -XGET "https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-1min" 
```

回應範例：

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
