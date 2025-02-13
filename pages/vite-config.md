
# Редактирование точки входа

<div style="flex: 1; display: flex;">

<div>

```js
const htmlPlugin = () => {
	return {
		name: 'html-transform',
		transformIndexHtml(html) {
			return html.replace(
				/<title>(.*?)<\/title>/,
				`<title>Title replaced!</title>`,
			)
		},
	}
}
```

</div>

<div class="center-col" style="gap: 32px; flex: 1;">

<QRCode
    :width="300"
    :height="300"
    type="svg"
    data="https://vite.dev/guide/api-plugin.html#transformindexhtml"
    :dotsOptions="{ type: 'rounded', color: 'white' }"
/>

## https://vite.dev/guide/api-plugin.html

</div>

</div>
