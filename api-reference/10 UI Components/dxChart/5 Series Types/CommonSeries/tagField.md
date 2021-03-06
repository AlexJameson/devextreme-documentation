---
id: dxChartSeriesTypes.CommonSeries.tagField
type: String
default: 'tag'
notUsedInTheme: 
---
---
##### shortDescription
Specifies which data source field provides auxiliary data for series points.

---
This property allows you to associate virtually any required data with a series point. This data will be stored in the [tag](/api-reference/10%20UI%20Components/BaseChart/7%20Chart%20Elements/Point/2%20Fields/tag.md '/Documentation/ApiReference/UI_Components/dxChart/Chart_Elements/Point/Fields/#tag') field of the [Point](/api-reference/10%20UI%20Components/dxChart/7%20Chart%20Elements/Point '/Documentation/ApiReference/UI_Components/dxChart/Chart_Elements/Point/') object.

Commonly, a chart contains several series, and many of them have the same **tagField** value. In this case, specify the **tagField** property in the **commonSeriesSettings** object. If a series must have a unique **tagField** value, specify the same property, but do so in the series object within the [series](/api-reference/10%20UI%20Components/dxChart/1%20Configuration/series '/Documentation/ApiReference/UI_Components/dxChart/Configuration/series/') array.

#####See Also#####
- **series**.[tag](/api-reference/10%20UI%20Components/dxChart/5%20Series%20Types/ChartSeries/tag.md '/Documentation/ApiReference/UI_Components/dxChart/Configuration/series/#tag') - associates data with an entire series.