# Reporting API v4

https://developers.google.com/analytics/devguides/reporting/core/v4/rest/v4/reports/batchGet

### 僅提供一種接口，依據不同參數獲得不同資料 (透過Google Analytics後台能看到的報表API也只能取得那些)
### 官方文檔：https://developers.google.com/analytics/devguides/reporting/core/v4/rest/v4/reports/batchGet#ReportRequest.FIELDS.date_ranges
### Google Analytics A 分為四種報表數據，請求接口相同參數不同
1. 總結報表 (查看指標的統計)
2. 數據透視報表 (查看指標的維度統計)
3. 同类群组報表 (beta階段，相同身分的階段群組)
4. 生命周期价值 (beta階段，這段時間頁面的廣告收益)

### 主要透過 metrics (指標)、 dimensions(維度)這兩個參數控制
1. metrics (指標)：用來統計數字，比如瀏覽次數、頁面廣告量等
2. dimensions(維度)：用來分組跟SQL的Group相似
### 參數類型可以來此網站查閱：https://ga-dev-tools.web.app/dimensions-metrics-explorer/

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

