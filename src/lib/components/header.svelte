<script lang="ts">
	import * as m from '$lib/paraglide/messages.js';
	import LocaleSwitcher from '$components/locale-switcher.svelte';
	import ThemeToggle from '$components/theme-toggle.svelte';
</script>

<header class="flex items-center justify-between py-4 border-b border-gray-200 dark:border-gray-700">
	<a href="/" class="text-xl font-semibold text-gray-900 dark:text-gray-100 hover:text-blue-600 dark:hover:text-blue-400 transition-colors">
		{m.house_patchy_flamingo_link()}
	</a>

	<div class="flex items-center gap-3">
		<ThemeToggle />
		<LocaleSwitcher />
	</div>
</header>
