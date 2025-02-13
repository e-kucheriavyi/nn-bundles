# Tree shaking

<v-click>

## main.js

```js
import { a, b, sum } from 'lib.js';

console.log(`${a()} + ${b()} = ${sum()}`);
```

</v-click>

<v-click>

<br>

## lib.js

````md magic-move
```js {all|1,3,7,9}
const a = () => 4;

const b = () => 2;

const c = () => 3;

const sum = () => a() + b();

export { a, b, c, sum };
```

```js
const a = () => 4;

const b = () => 2;

const sum = () => a() + b();

export { a, b, sum };
```
````

</v-click>

---
transition: fade
---

# Tree shaking

<br>
<br>
<br>
<br>
<br>

<div class="center-col" style="flex: 1;">

## <v-click>До минификации: 677.87 kB -> 470.31 kB</v-click> <span v-click class="green">~30%</span>

<br>

## <v-click>После минификации: 188.31 kB -> 186.86 kB</v-click> <span v-click class="red">~2%</span>

</div>
