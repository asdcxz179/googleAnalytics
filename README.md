# Reporting API v4

https://developers.google.com/analytics/devguides/reporting/core/v4/rest/v4/reports/batchGet

### 僅提供一種接口，依據不同參數獲得不同資料
### 官方文檔：https://developers.google.com/analytics/devguides/reporting/core/v4/rest/v4/reports/batchGet#ReportRequest.FIELDS.date_ranges
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
