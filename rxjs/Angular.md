Docs: https://angular.io/guide/rx-library

Recommended blog: https://blog.csdn.net/dongnihao/article/details/125890925

# Common operators

RxJS provides many operators, but only a handful are used frequently.

![Common Operations](/rxjs/img/rxjs-common-operations.png "Common Operations")

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

## fromEvent


