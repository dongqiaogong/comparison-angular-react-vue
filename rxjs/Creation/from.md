## from

Description: Converts almost anything to an Observable.

![from](/rxjs/img/from.png "from")

```javascript
import { from } from 'rxjs';

const array = [10, 20, 30];
const result = from(array);

result.subscribe(x => console.log(x));

// Logs:
// 10
// 20
// 30
```