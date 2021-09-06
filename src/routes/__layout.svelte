<script>
	import '../app.postcss';
	import Header from '$lib/components/Header.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import { isAuthenticated } from '$lib/store';
</script>

<svelte:head>
	<title>Energify</title>
	<link
		rel="icon"
		href="https://cdn.discordapp.com/attachments/883374253989298176/883784525421871184/energify-logos_black.png"
	/>
</svelte:head>

<Header />
<main>
	{#if !$isAuthenticated}
		<div class="bg-white dark:bg-gray-800 overflow-hidden relative lg:flex lg:items-center">
			<div class="w-full py-12 px-4 sm:px-6 lg:py-16 lg:px-8 z-20">
				<h2 class="text-3xl font-extrabold text-black dark:text-white sm:text-4xl">
					<span class="block"> Save the planet </span>
				</h2>
				<p class="text-md mt-4 text-gray-400">Motivational message</p>
			</div>
			<div class="flex items-center gap-8 p-8 lg:p-24">
				<img
					src="https://www.tailwind-kit.com/images/landscape/3.jpg"
					class="rounded-lg w-1/2"
					alt="Tree"
				/>
				<div>
					<img
						src="https://www.tailwind-kit.com/images/landscape/2.jpg"
						class="rounded-lg mb-8"
						alt="Tree"
					/>
					<img
						src="https://www.tailwind-kit.com/images/landscape/4.jpg"
						class="rounded-lg"
						alt="Tree"
					/>
				</div>
			</div>
		</div>

		<div class="sm:flex flex-wrap justify-center items-center text-center gap-8">
			<div
				class="w-full sm:w-1/2 md:w-1/2 lg:w-1/4 px-4 py-4 bg-white mt-6  shadow-lg rounded-lg dark:bg-gray-800"
			>
				<div class="flex-shrink-0">
					<div
						class="flex items-center mx-auto justify-center h-12 w-12 rounded-md bg-indigo-500 text-white"
					>
						<svg
							width="20"
							height="20"
							fill="currentColor"
							class="h-6 w-6"
							viewBox="0 0 1792 1792"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M491 1536l91-91-235-235-91 91v107h128v128h107zm523-928q0-22-22-22-10 0-17 7l-542 542q-7 7-7 17 0 22 22 22 10 0 17-7l542-542q7-7 7-17zm-54-192l416 416-832 832h-416v-416zm683 96q0 53-37 90l-166 166-416-416 166-165q36-38 90-38 53 0 91 38l235 234q37 39 37 91z"
							/>
						</svg>
					</div>
				</div>
				<h3 class="text-2xl sm:text-xl text-gray-700 font-semibold dark:text-white py-4">
					Example
				</h3>
				<p class="text-md  text-gray-500 dark:text-gray-300 py-4">a lot of text</p>
			</div>
			<div
				class="w-full sm:w-1/2 md:w-1/2 lg:w-1/4 px-4 py-4 mt-6 sm:mt-16 md:mt-20 lg:mt-24 bg-white shadow-lg rounded-lg dark:bg-gray-800"
			>
				<div class="flex-shrink-0">
					<div
						class="flex items-center mx-auto justify-center h-12 w-12 rounded-md bg-indigo-500 text-white"
					>
						<svg
							width="20"
							height="20"
							fill="currentColor"
							class="h-6 w-6"
							viewBox="0 0 1792 1792"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M491 1536l91-91-235-235-91 91v107h128v128h107zm523-928q0-22-22-22-10 0-17 7l-542 542q-7 7-7 17 0 22 22 22 10 0 17-7l542-542q7-7 7-17zm-54-192l416 416-832 832h-416v-416zm683 96q0 53-37 90l-166 166-416-416 166-165q36-38 90-38 53 0 91 38l235 234q37 39 37 91z"
							/>
						</svg>
					</div>
				</div>
				<h3 class="text-2xl sm:text-xl text-gray-700 font-semibold dark:text-white py-4">
					example
				</h3>
				<p class="text-md text-gray-500 dark:text-gray-300 py-4">a lot of text</p>
			</div>
			<div
				class="w-full sm:w-1/2 md:w-1/2 lg:w-1/4 mt-6  px-4 py-4 bg-white shadow-lg rounded-lg dark:bg-gray-800"
			>
				<div class="flex-shrink-0">
					<div
						class="flex items-center mx-auto justify-center h-12 w-12 rounded-md bg-indigo-500 text-white"
					>
						<svg
							width="20"
							height="20"
							fill="currentColor"
							class="h-6 w-6"
							viewBox="0 0 1792 1792"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M491 1536l91-91-235-235-91 91v107h128v128h107zm523-928q0-22-22-22-10 0-17 7l-542 542q-7 7-7 17 0 22 22 22 10 0 17-7l542-542q7-7 7-17zm-54-192l416 416-832 832h-416v-416zm683 96q0 53-37 90l-166 166-416-416 166-165q36-38 90-38 53 0 91 38l235 234q37 39 37 91z"
							/>
						</svg>
					</div>
				</div>
				<h3 class="text-2xl sm:text-xl text-gray-700 font-semibold dark:text-white py-4">
					example
				</h3>
				<p class="text-md  text-gray-500 dark:text-gray-300 py-4">a lot of text</p>
			</div>
		</div>
	{:else}
		<slot />
		<script src="https://apps.elfsight.com/p/platform.js" defer></script>
		<div class="elfsight-app-cdfba14e-c728-4c7e-8ce6-8a4cefd13e0c" />
	{/if}
</main>
<Footer />
