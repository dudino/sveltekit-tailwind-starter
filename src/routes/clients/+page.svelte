<script lang="ts">
	import { mode } from 'mode-watcher';
</script>

<svelte:head>
	<title>Dark Theme Test Page</title>
</svelte:head>

<div class="space-y-8">
	<!-- Header Section -->
	<div class="text-center">
		<h1 class="text-4xl font-bold text-gray-900 dark:text-gray-100 mb-4">
			Dark Theme Test Page
		</h1>
		<p class="text-lg text-gray-600 dark:text-gray-300 mb-6">
			Test all the dark theme features and components
		</p>
		
		<!-- Current Theme Display -->
		<div class="inline-flex items-center px-4 py-2 rounded-lg bg-blue-100 dark:bg-blue-900 text-blue-800 dark:text-blue-200">
			<span class="font-medium">Current theme: {$mode || 'loading...'}</span>
		</div>
	</div>

	<!-- Theme Demo Cards -->
	<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
		<!-- Card 1: Basic Colors -->
		<div class="bg-white dark:bg-gray-800 rounded-lg shadow-lg p-6 border border-gray-200 dark:border-gray-700">
			<h3 class="text-xl font-semibold text-gray-900 dark:text-gray-100 mb-3">Basic Colors</h3>
			<p class="text-gray-600 dark:text-gray-300 mb-4">
				This card demonstrates basic text and background colors in both light and dark modes.
			</p>
			<div class="space-y-2">
				<div class="text-sm text-gray-500 dark:text-gray-400">Secondary text</div>
				<div class="text-xs text-gray-400 dark:text-gray-500">Muted text</div>
			</div>
		</div>

		<!-- Card 2: Interactive Elements -->
		<div class="bg-white dark:bg-gray-800 rounded-lg shadow-lg p-6 border border-gray-200 dark:border-gray-700">
			<h3 class="text-xl font-semibold text-gray-900 dark:text-gray-100 mb-3">Interactive Elements</h3>
			<div class="space-y-3">
				<button class="w-full px-4 py-2 bg-blue-600 hover:bg-blue-700 text-white rounded-md transition-colors">
					Primary Button
				</button>
				<button class="w-full px-4 py-2 border border-gray-300 dark:border-gray-600 text-gray-700 dark:text-gray-300 hover:bg-gray-50 dark:hover:bg-gray-700 rounded-md transition-colors">
					Secondary Button
				</button>
				<input 
					type="text" 
					placeholder="Test input field"
					class="w-full px-3 py-2 border border-gray-300 dark:border-gray-600 rounded-md bg-white dark:bg-gray-700 text-gray-900 dark:text-gray-100 placeholder-gray-500 dark:placeholder-gray-400"
				/>
			</div>
		</div>

		<!-- Card 3: Status Indicators -->
		<div class="bg-white dark:bg-gray-800 rounded-lg shadow-lg p-6 border border-gray-200 dark:border-gray-700">
			<h3 class="text-xl font-semibold text-gray-900 dark:text-gray-100 mb-3">Status Indicators</h3>
			<div class="space-y-3">
				<div class="flex items-center space-x-2">
					<div class="w-3 h-3 bg-green-500 rounded-full"></div>
					<span class="text-green-600 dark:text-green-400">Success</span>
				</div>
				<div class="flex items-center space-x-2">
					<div class="w-3 h-3 bg-yellow-500 rounded-full"></div>
					<span class="text-yellow-600 dark:text-yellow-400">Warning</span>
				</div>
				<div class="flex items-center space-x-2">
					<div class="w-3 h-3 bg-red-500 rounded-full"></div>
					<span class="text-red-600 dark:text-red-400">Error</span>
				</div>
			</div>
		</div>
	</div>

	<!-- Code Block Example -->
	<div class="bg-white dark:bg-gray-800 rounded-lg shadow-lg p-6 border border-gray-200 dark:border-gray-700">
		<h3 class="text-xl font-semibold text-gray-900 dark:text-gray-100 mb-4">Code Example</h3>
		<pre class="bg-gray-100 dark:bg-gray-900 rounded-md p-4 overflow-x-auto">
			<code class="text-sm text-gray-800 dark:text-gray-200">
{`// Example of dark theme implementation
import { mode, toggleMode } from 'mode-watcher';

function handleThemeToggle() {
  toggleMode();
  console.log('Theme changed to:', $mode);
}`}
			</code>
		</pre>
	</div>

	<!-- Navigation Links -->
	<div class="bg-white dark:bg-gray-800 rounded-lg shadow-lg p-6 border border-gray-200 dark:border-gray-700">
		<h3 class="text-xl font-semibold text-gray-900 dark:text-gray-100 mb-4">Navigation Links</h3>
		<nav class="space-y-2">
			<a href="/" class="block text-blue-600 dark:text-blue-400 hover:text-blue-800 dark:hover:text-blue-300 transition-colors">
				← Back to Home
			</a>
			<a href="/appointments" class="block text-blue-600 dark:text-blue-400 hover:text-blue-800 dark:hover:text-blue-300 transition-colors">
				Appointments
			</a>
			<a href="/staff" class="block text-blue-600 dark:text-blue-400 hover:text-blue-800 dark:hover:text-blue-300 transition-colors">
				Staff
			</a>
			<a href="/reports" class="block text-blue-600 dark:text-blue-400 hover:text-blue-800 dark:hover:text-blue-300 transition-colors">
				Reports
			</a>
		</nav>
	</div>

	<!-- Instructions -->
	<div class="bg-blue-50 dark:bg-blue-900/20 border border-blue-200 dark:border-blue-800 rounded-lg p-6">
		<h3 class="text-lg font-semibold text-blue-900 dark:text-blue-100 mb-2">How to Test</h3>
		<ul class="list-disc list-inside space-y-1 text-blue-800 dark:text-blue-200">
			<li>Click the theme toggle button in the header (moon/sun icon)</li>
			<li>Notice how all colors, backgrounds, and text adapt to the new theme</li>
			<li>Try interacting with buttons and input fields</li>
			<li>The theme preference is automatically saved in localStorage</li>
			<li>Refresh the page to confirm persistence</li>
		</ul>
	</div>
</div>
