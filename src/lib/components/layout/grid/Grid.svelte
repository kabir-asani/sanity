<script lang="ts">
	import { GridVariant } from './Grid';

	export let variant: GridVariant = GridVariant.row;
</script>

<div
	class={'grid' +
		' ' +
		(variant == GridVariant.row ? 'grid-flow-row' : 'grow-flow-col') +
		' ' +
		($$restProps.class || '')}
>
	<slot />
</div>
