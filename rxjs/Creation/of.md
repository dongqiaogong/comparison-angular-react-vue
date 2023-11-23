## of 

 Description: Each argument becomes a next notification.

 ![of](/rxjs/img/of.png "of")

 ```javascript
 import { of } from 'rxjs';
 
of(10, 20, 30)
  .subscribe({
    next: value => console.log('next:', value),
    error: err => console.log('error:', err),
    complete: () => console.log('the end'),
  });
 
// Outputs
// next: 10
// next: 20
// next: 30
// the end
 ```

 Note: see the different between 'from' and 'of'

```javascript
import { from } from 'rxjs';

const array = [10, 20, 30];
const result = of(array);

result.subscribe(x => console.log(x));

// Logs:
// [10, 20, 30]
```