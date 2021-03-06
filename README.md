[![Build Status](https://semaphoreci.com/api/v1/netanel7799/ngx-stop-propagation/branches/master/badge.svg)](https://semaphoreci.com/netanel7799/ngx-stop-propagation)
### ✋ Stop propagation for everyday events with Angular directives 🎩

#### Installation

To install this library, run:

```bash
$ npm install ngx-stop-propagation --save
```
```js
import { StopPropagationModule } from 'ngx-stop-propagation';

@NgModule({
  imports: [
    StopPropagationModule
  ]
})
export class AppModule { }
```

### Usage
- `(click.stop)` - The click event's propagation will be stopped
```html
  <button (click.stop)="onClick($event, extraData)">Click Me!!</button>
```
- `(change.stop)` - The change event's propagation will be stopped
```html
  <input (change.stop)="onChange($event, extraData)">
```
- `(mouseover.stop)` - The mouseover event's propagation will be stopped
```html
  <div (mouseover.stop)="onChange($event, extraData)"></div>
```
- `(mouseenter.stop)` - The mouseover event's propagation will be stopped
```html
  <div (mouseenter.stop)="onChange($event, extraData)"></div>
```

You can also pass `[eventOptions]`:
```html
  <div (click.stop)="onClick($event, extraData)"
       [eventOptions]="{preventDefault: true}">
     <button>Click Me!!</button>
  </div>
```
## License

MIT © [Netanel Basal](mailto:netanel7799@gmail.com)
