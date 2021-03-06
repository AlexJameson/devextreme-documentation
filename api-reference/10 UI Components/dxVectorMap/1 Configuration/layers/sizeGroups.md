---
id: dxVectorMap.Options.layers.sizeGroups
type: Array<Number>
default: undefined
---
---
##### shortDescription
Allows you to display [bubbles](/api-reference/10%20UI%20Components/dxVectorMap/1%20Configuration/layers/elementType.md '/Documentation/ApiReference/UI_Components/dxVectorMap/Configuration/layers/#elementType') with similar attributes in the same size. Setting this property makes sense only if the [layer type](/api-reference/10%20UI%20Components/dxVectorMap/1%20Configuration/layers/type.md '/Documentation/ApiReference/UI_Components/dxVectorMap/Configuration/layers/#type') is *"marker"* and the [elementType](/api-reference/10%20UI%20Components/dxVectorMap/1%20Configuration/layers/elementType.md '/Documentation/ApiReference/UI_Components/dxVectorMap/Configuration/layers/#elementType') is *"bubble"*.

---
If you have specified the [field that provides marker-sizing data](/api-reference/10%20UI%20Components/dxVectorMap/1%20Configuration/layers/sizeGroupingField.md '/Documentation/ApiReference/UI_Components/dxVectorMap/Configuration/layers/#sizeGroupingField'), you need to specify groups into which this data must be classified. For this purpose, assign an array of numbers to the [sizeGroups](/api-reference/10%20UI%20Components/dxVectorMap/1%20Configuration/layers/sizeGroups.md '/Documentation/ApiReference/UI_Components/dxVectorMap/Configuration/layers/#sizeGroups') property. Each pair of numbers in this array defines a range of data values.

For example, consider that the **sizeGroups** array contains four items: [0, 1, 2, 3]. This array specifies three ranges, or groups: 0-1, 1-2 and 2-3. Thus, data values will be split up into three groups. Each group will be assigned a size correlating with the group values. This size will be calculated automatically taking into account the [minSize](/api-reference/10%20UI%20Components/dxVectorMap/1%20Configuration/layers/minSize.md '/Documentation/ApiReference/UI_Components/dxVectorMap/Configuration/layers/#minSize') and [maxSize](/api-reference/10%20UI%20Components/dxVectorMap/1%20Configuration/layers/maxSize.md '/Documentation/ApiReference/UI_Components/dxVectorMap/Configuration/layers/#maxSize') values. Markers of those data values that do not match neither group will have a default size.