nxtlife-ionic2-rating
======================

Build a simple directive to visualize a star rating bar using angular2 and ionic2.

[![NPM version][npm-image]][npm-url] [![Downloads][downloads-image]][downloads-url]

[![NPM][nodei-image]][nodei-url]

## How to install:

```
$ npm install --save nxtlife-ionic2-rating
```

## How to use:

Import `NxtLifeIonic2RatingModule` on module definition that declares the page where you want to add the rating component.
In some cases, all pages are declared on `src/app/app.module.ts`.

```typescript
import { NgModule } from '@angular/core';
import { IonicApp, IonicModule } from 'ionic-angular';
import { MyApp } from './app.component';
import { HomePage } from '../pages/home/home';

// Import ionic2-rating module
import { NxtLifeIonic2RatingModule } from 'nxtlife-ionic2-rating';

@NgModule({
  declarations: [
    MyApp,
    HomePage
  ],
  imports: [
    IonicModule.forRoot(MyApp),
    NxtLifeIonic2RatingModule // Put ionic2-rating module here
  ],
  bootstrap: [IonicApp],
  entryComponents: [
    MyApp,
    HomePage
  ],
  providers: []
})
export class AppModule {}
```

Include the component on page template, like the example below:
```HTML
<nxtlife-rating [(ngModel)]="rate" 
        readOnly="false" <!--default value-->
        max="5" <!--default value-->
        emptyStarIconName="star-outline" <!--default value-->
        halfStarIconName="star-half" <!--default value-->
        starIconName="star" <!--default value-->
        nullable="false" <!--default value-->
        (ngModelChange)="onModelChange($event)"> <!--use it when you need to do something when user clicks on a star. in case you only need to change ngModel property, this property can be ommited.-->
</nxtlife-rating>
```

### You may also need to customize component styles:

```CSS
ul {
  padding: 0px;

  &.rating li {
    padding: 5px 10px !important;
    background: none;
    color: #ffb400;

    ion-icon {
      font-size: 30px;
    }
  }
}
```


[npm-url]: https://www.npmjs.com/package/nxtlife-ionic2-rating
[downloads-url]: http://badge.fury.io/js/nxtlife-ionic2-rating
[npm-image]: https://img.shields.io/npm/v/nxtlife-ionic2-rating.svg
[downloads-image]: https://img.shields.io/npm/dm/nxtlife-ionic2-rating.svg
[nodei-image]: https://nodei.co/npm/nxtlife-ionic2-rating.png?downloads=true&downloadRank=true&stars=true
[nodei-url]: https://www.npmjs.com/package/nxtlife-ionic2-rating