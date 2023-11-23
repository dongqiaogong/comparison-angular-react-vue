## fromEvent

Description: Creates an Observable from DOM events, or Node.js EventEmitter events or others.

![fromEvent](/rxjs/img/fromEvent.png "fromEvent")

```javascript
import { fromEvent } from 'rxjs';

const clicks = fromEvent(document, 'click');
clicks.subscribe(x => console.log(x));

// Results in:
// MouseEvent object logged to console every time a click
// occurs on the document.
```

Note: 
 - fromEvent is almost likely addEventHandler, it also have bubble(down to up) and capture(up to down)
 - When Observable is unsubscribed, function will be unregistered from event target.