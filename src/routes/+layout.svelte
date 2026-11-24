<script lang="ts">
	import DemoLinks from './demo/DemoLinks.svelte';
	import './layout.css';
	import favicon from '#lib/assets/favicon.svg';
	import { DarkMode } from 'flowbite-svelte';
	import type { LayoutProps } from './$types';

	let { children }: LayoutProps = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<header
	class="flex items-center justify-between border-b border-gray-200 bg-white px-4 py-3 dark:border-gray-700 dark:bg-gray-900"
>
	<span class="text-lg font-semibold text-gray-900 dark:text-white">nonsense</span>
	<DarkMode class="rounded-lg text-gray-500 hover:bg-gray-100 dark:text-gray-400 dark:hover:bg-gray-700" />
</header>

<main class="bg-white text-gray-900 dark:bg-gray-900 dark:text-white">
	{@render children()}
	<DemoLinks />
</main>
