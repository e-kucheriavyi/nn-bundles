<template>
	<div class="slidev-layout default">
		<div :class="$style.container">
			<div style="flex: 1;">
				<slot />
			</div>
		</div>
	</div>
</template>

<style module>
	.container {
		height: 100%;
		width: 100%;
		display: flex;
		flex: 1;
		flex-direction: column;
	}
</style>
