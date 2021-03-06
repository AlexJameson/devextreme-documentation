DevExtreme provides the <a href="https://github.com/DevExpress/DevExtreme.AspNet.Data/blob/master/README.md" target="_blank">DevExtreme.AspNet.Data</a> extension to access an ASP.NET Web API service. This extension consists of two parts: the server-side part implements data processing on the server according to the protocol the SelectBox uses; the client-side part creates and configures a [CustomStore](/api-reference/30%20Data%20Layer/CustomStore '/Documentation/ApiReference/Data_Layer/CustomStore/') to access the server from the client. The following code shows how to use the extension's client-side <a href="https://github.com/DevExpress/DevExtreme.AspNet.Data/blob/master/docs/client-side-with-jquery.md#api-reference" target="_blank">createStore</a> method.

---
##### jQuery

    <!--JavaScript-->
    $(function() {
        const serviceUrl = "http://url/to/my/service";
        $("#selectBoxContainer").dxSelectBox({
            dataSource: DevExpress.data.AspNet.createStore({
                key: "ID",
                loadUrl: serviceUrl + "/GetAction",
                insertUrl: serviceUrl + "/InsertAction"
            }),
            // ...
        })
    });

##### Angular

    <!--TypeScript-->
    import { DxSelectBoxModule } from "devextreme-angular";
    import CustomStore from "devextreme/data/custom_store";
    import { createStore } from "devextreme-aspnet-data-nojquery";
    // ...
    export class AppComponent {
        store: CustomStore;
        constructor() {
            let serviceUrl = "http://url/to/my/service";
            this.store = createStore({
                key: "ID",
                loadUrl: serviceUrl + "/GetAction",
                insertUrl: serviceUrl + "/InsertAction"
            })
        }
    }
    @NgModule({
        imports: [
            // ...
            DxSelectBoxModule
        ],
        // ...
    })

    <!--HTML-->
    <dx-select-box ...
        [dataSource]="store">
    </dx-select-box>

---