<script lang="ts">
	import { onMount, onDestroy } from 'svelte';

	let screenWidth: number;

	// Function to determine the screen size
	function updateScreenWidth() {
		screenWidth = window.innerWidth;
	}

	onMount(() => {
		updateScreenWidth();
		window.addEventListener('resize', updateScreenWidth);
		return () => {
			window.removeEventListener('resize', updateScreenWidth);
		};
	});
</script>

<!-- Mobile Slot -->
{#if screenWidth < 768}
	<slot name="mobile" />
{/if}

<!-- Tablet Slot -->
{#if screenWidth >= 768 && screenWidth <= 1280}
	<slot name="tablet" />
{/if}

<!-- Desktop Slot -->
{#if screenWidth > 1280}
	<slot name="desktop" />
{/if}
