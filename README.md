# Reporting API v4

https://developers.google.com/analytics/devguides/reporting/core/v4/rest/v4/reports/batchGet

### 僅提供一種接口，依據不同參數獲得不同資料 (透過Google Analytics後台能看到的報表API也只能取得那些)
### 官方文檔：https://developers.google.com/analytics/devguides/reporting/core/v4/rest/v4/reports/batchGet#ReportRequest.FIELDS.date_ranges
### Google Analytics 分為四種報表數據
1. 總結報表
2. 數據透視報表
3. 同类群组報表
4. 生命周期价值

### 主要透過 metrics (指標)、 dimensions(維度)這兩個參數控制

### 共通參數
```json
{
	"viewId": 123455//視圖ＩＤ,
	"dateRanges": [
		{
			"startDate": "2022-08-01",
			"endDate": "2022-08-07"
		}
	],
	"dimensions": [
		{
			"name": "ga:browser",
		}
	],
	"metrics": [
		{
			"expression": "ga:users",
		}
	]
}
```

