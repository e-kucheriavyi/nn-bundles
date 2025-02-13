# Sourcemap

<div style="flex:1; display: flex; gap: 32px">

<div style="flex: 1;">

<v-click>

## inline: <span class="red">1 519.53 kB</span>

<br>

```js
// vite.config.js
export default defineConfig({
	build: {
		sourcemap: 'inline',
	},
})
```

</v-click>

</div>

<div>

<v-click>

## hidden: <span class="green">186.86 kB</span> (997.86 kB)

<br>

```js
// vite.config.js
export default defineConfig({
	build: {
		sourcemap: 'hidden',
	},
})
```

</v-click>

</div>

</div>

<br>
<br>
<br>
<br>

<v-click>

> Sourcemap генерируется для каждого чанка

</v-click>
