# Dev - FE - Dashboard & Widgets

## Directory Structure

```text
+ src/
   + component/
      + dashboard-component/
         + strategies/
            - dashboard-1x.strategy.ts
            - dashboard-2x.strategy.ts
         + widgets/
            + clock-widget/
               ...
            + stock-trading-widget/
               ...
            + weather-widget/
               ...
```

## Dashboard

Dashboard has 2 properties:

* A strategy that dictates how the dashboard widgets should be layout. It can be a 1 column strategy, which layout dashboard wigets in single column or a 2 columns strategy, which layout dashboard wigets in 2 columns or it can be something entirely different
* A bunch of dashboard wigets that could be dragged and drop on to the dashboard. Each widgets can be created multiple times, eg Widget1 for example can be drop 2 times creating widgets of different instance but all are of Widget1 type.

### Current Available Dashboard Strategies

#### dashboard-1x.strategy.ts

A single column dashboard strategy

![](../../../.gitbook/assets/dashboard-strategy-1x.png)

#### dashboard-2x.strategy.ts

A 2 columns dashboard strategy

![](../../../.gitbook/assets/dashboard-strategy-2x.png)

### Creating a new Dashboard Strategy

1\) Create a custom dashboard strategy file with a class that Implements `DashboardStrategy` as follows:

```text
export class MyDashboardStrategy implements DashboardStrategy {

   columnIndexes(): number[] {                                          // (1)
      // return the indexes of columns this strategy has
   }
   
   getDashboardWidgetInstancesForColumn(columnIndex: number):            // (2)
         DashboardWidgetInstance[] {
      // return the widget instance for this column index   
   }
   
   addDashboardWidgetInstances(                                          // (3)
         serializeInstanceFormats: 
             SerializeDashboardWidgetInstanceFormat[]) {
      // add this serialized dashboard instance to this 
      // dashboard
   }
   
   removeDashboardWidgetInstances(instanceIds: string[]) {               // (4)
      // remove the given dashbord widget instances identified
      // by the given instance ids
   }
   
   moveDashboardWidgetInstances(columnIndex: number,                     // (5)
        previousIndex: number, currentIndex: number) {
      // move a dashboard widget in this column identified by 
      // the columnIndex, from previous index in this column 
      // (previousIndex) to a new index (currentIndex). This is 
      // basically moving widget in the same column.
   }
   
   transferDashboardWidgetInstances(previousColumnIndex: number,         // (6)
        currentColumnIndex: numbner, previousIndex: number, 
        currentIndex: number) {
      // this is basically moving Widget from a column to a different
      // column, from previousColumnIndex to currentColumnIndex.
      // The widget is in previousIndex in previous column and in 
      // currentIndex in the current column
   }
   
   serialize(): string {                                                 // (7)
      // serialize this dashboard for saving purposes. It should
      // be able to reconstruct the dashboard based on the 
      // return string at later stage
   }
   
   deserialize(data: string) {                                            // (8)
      // deserialize this dashboard from the given serialized data
   }
}
```

#### Point \(1\)

return the indexes of columns this strategy has.

#### Point \(2\)

return the widget instance for this column index  

#### Point \(3\)

add this serialized dashboard instance to this dashboard

#### Point \(4\)

remove the given dashbord widget instances identified by the given instance ids

#### Point \(5\)

move a dashboard widget in this column identified by the columnIndex, from previous index in this column \(previousIndex\) to a new index \(currentIndex\). This is basically moving widget in the same column.

#### Point \(6\)

this is basically moving Widget from a column to a different column, from previousColumnIndex to currentColumnIndex. The widget is in previousIndex in previous column and in currentIndex in the current column

#### Point \(7\)

serialize this dashboard for saving purposes. It should be able to reconstruct the dashboard based on the return string at later stage

#### Point \(8\)

deserialize this dashboard from the given serialized data

2\) Place custom dashboard strategy file in `src/component/dashboard-component/strategies` directory.

3\) Register strategy by adding it to `DASHBOARD_STRATEGIES` constant field in  `src/component/dashboard-component/strategies/index.ts` 

```text
export const DASHBOARD_STRATEGIES = [
   ....
   new MyDashboardStrategy()
];
```

### Creating a new Dashboard Widget

1\) Create a custom dashboard widget file with a class that extends `DashboardWidget` as follows :

{% hint style="info" %}
As this is a normal angular widget, you can implements `OnInit`, `OnDestroy` or any other angular component lifecycle interfaces
{% endhint %}

```text
@Component({
    templateUrl: './my-widget.component.html',
    styleUrls: ['./my-widget.component.scss']
})
export class MyWidgetComponent extends DashboardWidget {

    static info(): DashboardWidgetInfo {                                // (1)
        return { 
            id: 'my-widget', 
            name: 'my-widget', 
            type: MyWidgetComponent 
        };
    }

    constructor(dashboardWidgetService: DashboardWidgetService) {      // (2)
        super(dashboardWidgetService);
    }

    loadClicked() {                                                    // (3)
        this.dashboardWidgetService.loadData()
          .pipe((tap(data: DataMap) => {
             // data loaded
          }).subscribe();
    }

    saveClicked() {                                                    // (4)
        const data: DataMap = {
           myData1: 'myDataValue1',
           myData2: 'myDataValue2'
        };
        this.dashboardWidgetService.saveData(data)
           .pipe((tap(r: ApiResponse) => {
              if (r.status === 'SUCCESS') {
                 // data saved
              }
           }).subscribe();
    }    
}
```

#### Point \(1\)

Create a `static info()` function returning a `DashboardWidgetInfo` object containing static info about the widget

| Properties | Description |
| :--- | :--- |
| id |  |
| name |  |
| type |  |

#### Point \(2\)

Stick in constructor with dependencies \(`DashboardWidgetService`\) that superclass `DashboardWidget` required.

{% hint style="info" %}
`DashboardWidgetService` is scoped in such a way that every `DashboardWidget` will have a copy of a separate instace so that it can contain information specific to this `DashboardWidget` eg. `instanceId`, current `User` etc.
{% endhint %}

#### Point \(3\)

One can load data for this widget instance through `DashboardWidgetService` `loadData()` function returning an `Observable<DataMap>`

#### Point \(4\)

One can save data for this widget instance through `DashboardWidgetService` `saveData(data)` function where data is of type `DataMap`, returning an `Observable<ApiResponse>`.

2\) Place custom dashboard widget file in `src/component/dashboard-component/widgets/<widget-name>` directory, where `<widget-name>` in this case is your widget name eg. `my-widget-component` together will all the artifacts the components need eg. the html template and scss files just like any other Angular components would require.

3\) Register strategy by adding it to `DASHBOARD_WIDGET_INFOS` constant field in  `src/component/dashboard-component/widgets/index.ts` 

```text
export const DASHBOARD_WIDGET_INFOS = [
    ...
    MyWidgetComponent.info(),
    ...
];

```



