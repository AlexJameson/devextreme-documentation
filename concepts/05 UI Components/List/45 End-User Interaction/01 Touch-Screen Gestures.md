The List supports the following touch-screen gestures.

- **Swipe**     
Swipe can be used to [delete an item](/concepts/05%20UI%20Components/List/35%20Item%20Deletion/01%20User%20Interaction.md '/Documentation/Guide/UI_Components/List/Item_Deletion/#User_Interaction') or access the commands of the [context menu](/concepts/05%20UI%20Components/List/40%20Item%20Context%20Menu.md '/Documentation/Guide/UI_Components/List/Item_Context_Menu/'). Performing this gesture raises the [itemSwipe](/api-reference/10%20UI%20Components/dxList/4%20Events/itemSwipe.md '/Documentation/ApiReference/UI_Components/dxList/Events/#itemSwipe') event. To handle it, assign a function to the [onItemSwipe](/api-reference/10%20UI%20Components/dxList/1%20Configuration/onItemSwipe.md '/Documentation/ApiReference/UI_Components/dxList/Configuration/#onItemSwipe') property, or subscribe to this event using the [on(eventName, eventHandler)](/api-reference/10%20UI%20Components/Component/3%20Methods/on(eventName_eventHandler).md '/Documentation/ApiReference/UI_Components/dxList/Methods/#oneventName_eventHandler') method.

    ---
    ##### jQuery

        <!--JavaScript-->
        $(function() {
            $("#listContainer").dxList({
                // ...
                onItemSwipe: function(e) {
                    // Event handling commands go here
                }
            });
        });

    <!-->

        <!--JavaScript-->
        const itemSwipeEventHandler1 = function(e) {
            // First handler of the "itemSwipe" event
        }
        const itemSwipeEventHandler2 = function(e) {
            // Second handler of the "itemSwipe" event
        }
        $("#listContainer").dxList("instance")
            .on("itemSwipe", itemSwipeEventHandler1)
            .on("itemSwipe", itemSwipeEventHandler2)

    ##### Angular

        <!--HTML-->
        <dx-list ...
            (onItemSwipe)="onItemSwipe($event)">
        </dx-list>

        <!--TypeScript-->
        import { DxListModule } from "devextreme-angular";
        // ...
        export class AppComponent {
            onItemSwipe (e) {
                // Event handling commands go here
            }
        }
        @NgModule({
            imports: [
                // ...
                DxListModule
            ],
            // ...
        })

    ---

- **Long Tap**      
Long tap can be used to access the commands of the [context menu](/concepts/05%20UI%20Components/List/40%20Item%20Context%20Menu.md '/Documentation/Guide/UI_Components/List/Item_Context_Menu/'). Performing this gesture raises the [itemHold](/api-reference/10%20UI%20Components/dxList/4%20Events/itemHold.md '/Documentation/ApiReference/UI_Components/dxList/Events/#itemHold') event. To handle it, assign a function to the [onItemHold](/api-reference/10%20UI%20Components/dxList/1%20Configuration/onItemHold.md '/Documentation/ApiReference/UI_Components/dxList/Configuration/#onItemHold') property, or subscribe to this event using the [on(eventName, eventHandler)](/api-reference/10%20UI%20Components/Component/3%20Methods/on(eventName_eventHandler).md '/Documentation/ApiReference/UI_Components/dxList/Methods/#oneventName_eventHandler') method just like it is demonstrated for the swipe gesture earlier on.

    You can also specify the time period the UI component should wait before raising the **itemHold** event. For this purpose, change the [itemHoldTimeout](/api-reference/10%20UI%20Components/CollectionWidget/1%20Configuration/itemHoldTimeout.md '/Documentation/ApiReference/UI_Components/dxList/Configuration/#itemHoldTimeout') property.

    ---
    ##### jQuery

        <!--JavaScript-->
        $(function() {
            $("#listContainer").dxList({
                // ...
                itemHoldTimeout: 1000 // the UI component will wait one second before raising the "itemHold" event 
            });
        });

    ##### Angular

        <!--HTML-->
        <dx-list ...
            [itemHoldTimeout]="1000"> <!-- the UI component will wait one second before raising the "itemHold" event -->
        </dx-list>

        <!--TypeScript-->
        import { DxListModule } from "devextreme-angular";
        // ...
        export class AppComponent {
            // ...
        }
        @NgModule({
            imports: [
                // ...
                DxListModule
            ],
            // ...
        })

    ---

- **Pull Down to Refresh**          
This gesture refreshes data in the List. To enable it, assign **true** to the [pullRefreshEnabled](/api-reference/10%20UI%20Components/dxList/1%20Configuration/pullRefreshEnabled.md '/Documentation/ApiReference/UI_Components/dxList/Configuration/#pullRefreshEnabled') property.

    ---
    ##### jQuery

        <!--JavaScript-->
        $(function() {
            $("#listContainer").dxList({
                // ...
                pullRefreshEnabled: true
            });
        });

    ##### Angular

        <!--HTML-->
        <dx-list ...
            [pullRefreshEnabled]="true">  
        </dx-list>

        <!--TypeScript-->
        import { DxListModule } from "devextreme-angular";
        // ...
        export class AppComponent {
            // ...
        }
        @NgModule({
            imports: [
                // ...
                DxListModule
            ],
            // ...
        })

    ---

    Performing this gesture raises the [pullRefresh](/api-reference/10%20UI%20Components/dxList/4%20Events/pullRefresh.md '/Documentation/ApiReference/UI_Components/dxList/Events/#pullRefresh') event. To handle it, assign a function to the [onPullRefresh](/api-reference/10%20UI%20Components/dxList/1%20Configuration/onPullRefresh.md '/Documentation/ApiReference/UI_Components/dxList/Configuration/#onPullRefresh') property, or subscribe to this event using the [on(eventName, eventHandler)](/api-reference/10%20UI%20Components/Component/3%20Methods/on(eventName_eventHandler).md '/Documentation/ApiReference/UI_Components/dxList/Methods/#oneventName_eventHandler') method just like it is demonstrated for the swipe gesture earlier on.

#####See Also#####
- [List - End-User Interaction | Universal Actions](/concepts/05%20UI%20Components/List/45%20End-User%20Interaction/05%20Universal%20Actions.md '/Documentation/Guide/UI_Components/List/End-User_Interaction/Universal_Actions/')
- [List - Localization](/concepts/05%20UI%20Components/List/50%20Localization.md '/Documentation/Guide/UI_Components/List/Localization/')
- [List Demos](https://js.devexpress.com/Demos/WidgetsGallery/Demo/List/ListEditingAndAPI)
- [List API Reference](/api-reference/10%20UI%20Components/dxList '/Documentation/ApiReference/UI_Components/dxList/')

[tags]list, touch-screen gestures, swipe, slide, onItemSwipe, long tap, long press, tap hold, onItemHold, itemHoldTimeout, pull down to refresh, pull to refresh, pullRefreshEnabled, onPullRefresh 