nxtlife-ionic2-rating
======================

Build a simple directive to visualize a star rating bar using angular2 and ionic2.

[![NPM version][npm-image]][npm-url] [![Downloads][downloads-image]][downloads-url]

[![NPM][nodei-image]][nodei-url]

## Installation:

```
$ npm install --save nxtlife-ionic2-rating
```

## Usage:

Import `NxtLifeIonic2RatingModule` on module definition that declares the page where you want to add the rating component.
In some cases, all pages are declared on `src/app/app.module.ts`.

```typescript
import { NgModule } from '@angular/core';
import { IonicModule } from 'ionic-angular';
import { MyApp } from './app.component';

// Import ionic2-rating module
import { NxtLifeIonic2RatingModule } from 'nxtlife-ionic2-rating';

@NgModule({
  ......
  ......
  imports: [
    IonicModule.forRoot(MyApp),
    NxtLifeIonic2RatingModule // Put ionic2-rating module here
  ],
  ......
  ......
})
export class AppModule {}
```

Include the component on page template, like the example below:
```HTML
<nxtlife-rating></nxtlife-rating>
```

### DEFAULT VALUE
```
readOnly = false,
max = 5,
emptyStarIconName = "star-outline",
halfStarIconName = "star-half",
starIconName = "star",
nullable = false
```
When you need to do something when user clicks on a start then you have to use `(click)` or `(ngModelChange)` with 
`[(ngModel)]`:

```HTML
<nxtlife-rating [(ngModel)]="rate" (ngModelChange)="onModelChange($event)">
</nxtlife-rating>
```

### If you want to customize style:

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
[npm-image]: https://img.shields.io/npm/v/nxtlife-ionic2-rating.svg
[nodei-image]: https://nodei.co/npm/nxtlife-ionic2-rating.png?downloads=true&downloadRank=true&stars=true
[nodei-url]: https://www.npmjs.com/package/nxtlife-ionic2-rating
[downloads-image]: https://img.shields.io/npm/dm/nxtlife-ionic2-rating.svg
[downloads-url]: http://badge.fury.io/js/nxtlife-ionic2-rating