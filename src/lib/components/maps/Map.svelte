<script lang="ts">
	import * as Card from '$lib/components/ui/card/index.js';
	import map1 from '$lib/assets/images/map1.png';

	const maps = [
		{
			title: 'Click to copy coordinates',
			description: 'March 30, 2026',
			image: map1,
			url: 'https://xinmiaooo.github.io/clicklatlng/'
		}
	];
</script>

<div class="container mx-auto px-4 py-8">
	<div class="grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
		{#each maps as map}
			<a href={map.url} target="_blank" rel="noopener noreferrer">
				<Card.Root class="overflow-hidden transition-shadow hover:shadow-lg">
					<img src={map.image} alt={map.title} class="h-48 w-full object-cover" />
					<Card.Header>
						<Card.Title>{map.title}</Card.Title>
						<Card.Description>{map.description}</Card.Description>
					</Card.Header>
				</Card.Root>
			</a>
		{/each}
	</div>
</div>
