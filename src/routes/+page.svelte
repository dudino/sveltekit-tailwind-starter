<script lang="ts">
	import * as m from '$lib/paraglide/messages.js';
	import { mode } from 'mode-watcher';
</script>

<svelte:head>
	<title>SvelteKit + TypeScript + TailwindCSS starter</title>
</svelte:head>

<div class="space-y-8">
	<div class="text-center">
		<h1 class="mt-0 text-4xl font-bold text-gray-900 dark:text-gray-100">
			{m.quiet_chunky_jay_empower({ name: 'SvelteKit' })}
		</h1>
		<p class="mt-4 text-lg text-gray-600 dark:text-gray-300">
			{@html m.fit_candid_spider_adore()}
		</p>
	</div>

	<!-- Theme Status -->
	<div class="max-w-2xl mx-auto">
		<div class="bg-gradient-to-r from-blue-50 to-indigo-50 dark:from-blue-900/20 dark:to-indigo-900/20 rounded-lg p-6 border border-blue-200 dark:border-blue-800">
			<h2 class="text-2xl font-semibold text-gray-900 dark:text-gray-100 mb-4">
				🌓 Dark Theme Enabled!
			</h2>
			<p class="text-gray-600 dark:text-gray-300 mb-4">
				Your application now supports both light and dark themes. The current theme is: 
				<strong class="text-blue-600 dark:text-blue-400">{$mode || 'loading...'}</strong>
			</p>
			<div class="space-y-2">
				<p class="text-sm text-gray-500 dark:text-gray-400">
					✅ Click the theme toggle in the header to switch themes
				</p>
				<p class="text-sm text-gray-500 dark:text-gray-400">
					✅ Theme preference is automatically saved
				</p>
				<p class="text-sm text-gray-500 dark:text-gray-400">
					✅ Respects system theme preference
				</p>
			</div>
		</div>
	</div>

	<!-- Quick Links -->
	<div class="max-w-2xl mx-auto">
		<div class="bg-white dark:bg-gray-800 rounded-lg shadow-lg p-6 border border-gray-200 dark:border-gray-700">
			<h3 class="text-xl font-semibold text-gray-900 dark:text-gray-100 mb-4">Test Pages</h3>
			<div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
				<a 
					href="/clients" 
					class="block p-4 bg-gray-50 dark:bg-gray-700 rounded-lg hover:bg-gray-100 dark:hover:bg-gray-600 transition-colors border border-gray-200 dark:border-gray-600"
				>
					<h4 class="font-medium text-gray-900 dark:text-gray-100">Dark Theme Test</h4>
					<p class="text-sm text-gray-600 dark:text-gray-300 mt-1">
						Comprehensive test page for all dark theme features
					</p>
				</a>
				<a 
					href="/appointments" 
					class="block p-4 bg-gray-50 dark:bg-gray-700 rounded-lg hover:bg-gray-100 dark:hover:bg-gray-600 transition-colors border border-gray-200 dark:border-gray-600"
				>
					<h4 class="font-medium text-gray-900 dark:text-gray-100">Appointments</h4>
					<p class="text-sm text-gray-600 dark:text-gray-300 mt-1">
						Appointment management page
					</p>
				</a>
			</div>
		</div>
	</div>
</div>
