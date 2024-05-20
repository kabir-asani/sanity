<script>
	import Container from '../container/Container.svelte';
	import Responsive from '../responsive/Responsive.svelte';
</script>

<Responsive>
	<Container slot="desktop" class="w-full max-w-6xl mx-auto">
		<slot />
	</Container>

	<Container slot="tablet" class="mx-12">
		<slot />
	</Container>

	<Container slot="mobile" class="mx-6">
		<slot />
	</Container>
</Responsive>
