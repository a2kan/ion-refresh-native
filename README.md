[![npm](https://img.shields.io/npm/l/ion-refresh-native.svg)](https://www.npmjs.com/package/ion-refresh-native/)
[![npm](https://img.shields.io/npm/v/ion-refresh-native.svg)](https://www.npmjs.com/package/ion-refresh-native/)
[![npm](https://img.shields.io/npm/dt/ion-refresh-native.svg)](https://www.npmjs.com/package/ion-refresh-native/)
[![npm](https://img.shields.io/npm/dm/ion-refresh-native.svg)](https://www.npmjs.com/package/ion-refresh-native/)

# Ion Refresh Native Directive

> This directive `ion-refresh-native` extends the functionality of the `ion-refresher` or the **Pull-To-Refresh** component of the Ionic Framework. This has been tested with Ionic v3.

### Installation ###
You can install the module from NPM using the following command.

`npm i ion-refresh-native --save` or `npm install ion-refresh-native --save`

### Usage ###
+ Import the Directive to your `app.module.ts`.
```typescript
import { NgModule } from '@angular/core';
...
import { IonRefreshNative } from 'ion-refresh-native';

@NgModule({
  declarations: [
	  ...
	  IonRefreshNative,
	  ...
  ],
  imports: [],
  bootstrap: [IonicApp],
  entryComponents: [],
  providers: []
})
export class AppModule {}
```
+ In your `app.scss` file, add the following:
```typescript
@import '../../node_modules/ion-refresh-native/dist/scss/ion-refresh-native';
```

### Implementation ###
+ Now add the `ion-refresh-native` attribute in the `ion-refresher` component.
+ Also specified `pullingIcon="ios-refresh-outline"` and `refreshingSpinner="crescent"` so the icons will just blend.
```html
<ion-content>

  <ion-refresher ion-refresh-native (ionRefresh)="doRefresh($event)">
    <ion-refresher-content pullingIcon="ios-refresh-outline" refreshingSpinner="crescent"></ion-refresher-content>
  </ion-refresher>

</ion-content>
```
### Notes ##
This is still in early stage. If any of you wants to help improve this module, please do send PR's.