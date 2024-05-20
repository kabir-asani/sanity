<script>
	import '../app.css';

	import { onMount } from 'svelte';
	import { updateThemeMode, watchThemeUpdates } from '$lib/utils';

	onMount(() => {
		updateThemeMode();
		watchThemeUpdates();
	});
</script>

<slot />
