<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.png';
	import * as NavigationMenu from '$lib/components/ui/navigation-menu/index.js';

	let { children } = $props();
</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>

<header
	class="border-b bg-pink-950 font-bold text-white"
	style="font-family: 'Caveat Variable', cursive;"
>
	<div class="container mx-auto flex items-center px-4 py-2">
		<NavigationMenu.Root>
			<NavigationMenu.List>
				<NavigationMenu.Item>
					<NavigationMenu.Link href="/">Map</NavigationMenu.Link>
				</NavigationMenu.Item>
				<NavigationMenu.Item>
					<NavigationMenu.Link href="/blog">Blog</NavigationMenu.Link>
				</NavigationMenu.Item>
				<NavigationMenu.Item>
					<NavigationMenu.Link href="/about">About</NavigationMenu.Link>
				</NavigationMenu.Item>
			</NavigationMenu.List>
		</NavigationMenu.Root>
	</div>
</header>

<main class="min-h-screen bg-pink-100">
	{@render children()}
</main>
