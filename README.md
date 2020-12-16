# Date Time Calendar

Date Time Calendar - Simple calendar to select date time.

## Getting Started


### Features

 - Max Date
 - Min Date
 - From - To Date selector
 - Max Range 

### Installing
Using `npm`:
```
npm i ng-datetime-calendar
```

### Implementation
1. Add __OwlDateTimeModule__ and __OwlNativeDateTimeModule__ to your __@NgModule__ like example below
    ```typescript
     import { NgModule } from '@angular/core';
     import { BrowserModule } from '@angular/platform-browser';
     import { MyTestApp } from './my-test-app';
    
     import { OwlDateTimeModule, OwlNativeDateTimeModule } from 'ng-datetime-calendar';
    
     @NgModule({
         imports: [ 
             BrowserModule, 
             OwlDateTimeModule, 
             OwlNativeDateTimeModule,
         ],
         declarations: [ MyTestApp ],
         bootstrap:    [ MyTestApp ]
     })
     export class MyTestAppModule {}
    ```
2.  Connecting a picker to an input and a trigger.

- For Single DatePicker Calendar
    ```html
   <input [(ngModel)]="selectedMoments" [owlDateTime]="datetimePicker" class="form-control" [max]="maxDate"
    [owlDateTimeTrigger]="datetimePicker" id="datesingle" />
    <owl-date-time [hour12Timer]=" true" [showSecondsTimer]="true" #datetimePicker></owl-date-time>
    ```

- For Range DatePicker Calendar
    ```html
    <input [(ngModel)]="selectedMoments" [selectMode]="'range'" [maxRange]="'3'"   [owlDateTimeTrigger]="date_range_component" [owlDateTime]="date_range_component" id="daterange">
    <owl-date-time #date_range_component></owl-date-time>
    ```
    
	
3 . Add styles. If you are using Angular CLI, you can add this to your styles.css:

		@import  '~ng-datetime-calendar/assets/style/picker.min.css';


## Dependencies

none

## License

none

## Reference

Angular Date Time Picker - https://www.npmjs.com/package/ng-pick-datetime

