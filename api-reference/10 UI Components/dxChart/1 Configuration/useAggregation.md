---
id: dxChart.Options.useAggregation
type: Boolean
dep: dxChartSeriesTypes.CommonSeries.aggregation.enabled
---
---
##### shortDescription
Specifies whether or not to filter the series points depending on their quantity.

---
By default, a chart displays all series points. But there may be situations when displaying all the series points may affect chart performance. In this case, it is better to aggregate the series points rather than display all of them. For this purpose, set the **useAggregation** property to **true**. The aggregation is based on the <a href="http://en.wikipedia.org/wiki/Median_filter" target="_blank">median filter</a> algorithm.