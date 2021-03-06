---
id: dxFormGroupItem.colCountByScreen
type: Object
inherits: ColCountResponsible
default: undefined
---
---
##### shortDescription
Specifies the relation between the [screen size qualifier](/api-reference/10%20UI%20Components/dxForm/1%20Configuration/screenByWidth.md '/Documentation/ApiReference/UI_Components/dxForm/Configuration/#screenByWidth') and the number of columns in the grouped layout.

---
---
##### jQuery

    <!--JavaScript-->
    $(function() {
        $("#formContainer").dxForm({
            // ...
            items: [{
                itemType: "group",
                items: [ ... ],
                colCountByScreen: {
                    xs: 2, 
                    sm: 3  
                }
            },
            // ...
            ]
        });
    });

##### Angular

    <!-- tab: app.component.html -->
    <dx-form ... >
        <dxi-item itemType="group">
            <dxo-col-count-by-screen 
                [xs]="2"  
                [sm]="3"> 
            </dxo-col-count-by-screen>
            <dxi-item ... ></dxi-item>
        </dxi-item>
    </dx-form>

    <!-- tab: app.module.ts -->
    import { BrowserModule } from '@angular/platform-browser';
    import { NgModule } from '@angular/core';
    import { AppComponent } from './app.component';

    import { DxFormModule } from 'devextreme-angular';

    @NgModule({
        declarations: [
            AppComponent
        ],
        imports: [
            BrowserModule,
            DxFormModule
        ],
        bootstrap: [AppComponent]
    })
    export class AppModule { }

---