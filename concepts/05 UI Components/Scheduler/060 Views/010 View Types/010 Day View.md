The **day** view displays appointments for a specified date. The Scheduler UI component arranges appointments from top to bottom. If their time intervals overlap, their width is decreased and they are placed next to each other.

![Day View](/images/UiWidgets/Scheduler_Day_View.png)

All-day appointments are displayed on the All-day panel. You can set an appointment limit on this panel using the [maxAppointmentsPerCell](/api-reference/10%20UI%20Components/dxScheduler/1%20Configuration/maxAppointmentsPerCell.md '/Documentation/ApiReference/UI_Components/dxScheduler/Configuration/#maxAppointmentsPerCell') property. Appointments that exceed this limit are hidden, and a [cell overflow indicator](/concepts/05%20UI%20Components/Scheduler/030%20Appointments/080%20Cell%20Overflow%20Indicator.md '/Documentation/Guide/UI_Components/Scheduler/Appointments/Cell_Overflow_Indicator/') is displayed instead. If hidden appointments are associated with the same resource, the indicator will have the same color as this resource. Otherwise, the indicator has a default color.

![Scheduler: Cell overflow indicator on a day view](/images/UiWidgets/scheduler-day-view-cell-overflow-indicator.png)

A user can click the cell overflow indicator to view the hidden appointments. 

![Drop-down List of Appointments](/images/UiWidgets/Scheduler_Day_DropDown_List.png)

Resource headers are displayed above the All-day panel when you [group appointments by resources](/concepts/05%20UI%20Components/Scheduler/040%20Resources/030%20Group%20Appointments%20by%20Resources.md '/Documentation/Guide/UI_Components/Scheduler/Resources/Group_Appointments_by_Resources/').

![Resource headers](/images/UiWidgets/Scheduler_Day_Resource_Headers.png)
