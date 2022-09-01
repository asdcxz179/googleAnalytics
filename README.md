# Reporting API v4

https://developers.google.com/analytics/devguides/reporting/core/v4/rest/v4/reports/batchGet

### 僅提供一種接口，依據不同參數獲得不同資料 (參數太多就不全部解釋，透過Google Analytics後台能看到的報表大部分都可以取得)
### 官方文檔：https://developers.google.com/analytics/devguides/reporting/core/v4/rest/v4/reports/batchGet#ReportRequest.FIELDS.date_ranges
### Google Analytics 分為四種報表數據
1. 總結報表
2. 數據透視報表
3. 同类群组報表
4. 生命周期价值

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
###
```json
	{
		viewId: 123455//視圖ＩＤ,
		dateRanges: [
			{
				startDate: "2022-08-01",
				endDate: "2022-08-07"
			}
		],
		samplingLevel: "DEFAULT"//樣本大小,
		dimensions: [
			{
				name: "ga:browser",
				histogramBuckets: [
					"<50"
				],
			}
		],
		dimensionFilterClauses: [
			{
				operator: "OR",
				filters: [
					{
					}
				],
			}
		],
		metrics: [
			{
				expression: "ga:users",
				alias: string,
				formattingType: enum(MetricType),
			}
		]
	}
```
