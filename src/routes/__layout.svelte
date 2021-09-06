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
					<span class="block"> Welcome to Energify. We’re here to help you make change in a sustainable way that benefits both you and the environment.  </span>
				</h2>
				<p class="text-md mt-4 text-gray-400">
					"The greatest threat to our planet is the belief that someone else will save it"
				</p>
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
					The Problem
				</h3>
				<p class="text-md  text-gray-500 dark:text-gray-300 py-4">
					The Intergovernmental Panel on Climate Change reports a predicted rise of 1.5 degrees C
					above industrial levels by 2030.
				</p>
				<p class="text-md  text-gray-500 dark:text-gray-300 py-4">Doesn't sound like a lot?</p>
				<p class="text-md  text-gray-500 dark:text-gray-300 py-4">
					This increase will pose a threat to health, livelihoods, food security, water supply,
					human security, and economic growth around the world.
				</p>
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
					Is it too late?
				</h3>
				<p class="text-md text-gray-500 dark:text-gray-300 py-4">
					To decrease global temperature increases, Co2 emissions need to decline by around 45% from
					2010 levels by 2030.
				</p>
				<p class="text-md  text-gray-500 dark:text-gray-300 py-4">
					Sure, this may sound like a lot.
				</p>
				<p class="text-md  text-gray-500 dark:text-gray-300 py-4">
					But, you can make an impact. You can help the earth, just by making a few small changes.
					Together, we will fight to ensure we don't destroy our precious home.
				</p>
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
					The Solution
				</h3>
				<p class="text-md  text-gray-500 dark:text-gray-300 py-4">
					No matter your race, gender, or nationality, all of us are in this fight together. It is
					neber too late to start changing the world.
				</p>
				<p class="text-md  text-gray-500 dark:text-gray-300 py-4">Welcome to Energify.</p>
				<p class="text-md  text-gray-500 dark:text-gray-300 py-4">
					We are here to help you make sustainable changes which benefit both you and the
					environment.
				</p>
			</div>
		</div>
	{:else}
		<slot />
	{/if}
</main>
<Footer />
