<script>
	let p, c, t;
	let count = 0;
	function incrementCount() {
		count += 1;
	}
	function handleSubmit() {
		let data = JSON.stringify(
			`{"kwh":${c},"price":${p},"type":${t}}`
		);
		console.log(data)
		fetch('http://8ac9-187-235-14-118.ngrok.io/response', {
			method: 'POST',
			body: data
		});
	}
</script>

<section class="m-6">
	<div>
		<div class="bg-white rounded-lg w-72 shadow block p-4 m-auto">
			<div class="w-full h-4 bg-gray-400 rounded-full mt-3">
				{#if count === 1}
					<div class="w-1/3 h-full text-center text-xs text-white bg-green-500 rounded-full">
						33%
					</div>
				{:else if count === 2}
					<div class="w-2/3 h-full text-center text-xs text-white bg-green-500 rounded-full">
						66%
					</div>
				{:else if count === 3}
					<div class="w-3/3 h-full text-center text-xs text-white bg-green-500 rounded-full">
						100%
					</div>
				{/if}
			</div>
		</div>
		<article>
			{#if count == 0}
				<div class="bg-white dark:bg-gray-800 ">
					<div class="text-center w-full mx-auto py-12 px-4 sm:px-6 lg:py-16 lg:px-8 z-20">
						<h2 class="text-3xl font-extrabold text-black dark:text-white sm:text-4xl">
							<span class="block"> Calculate your waste </span>
							<span class="block text-indigo-500"> reduce the price of your energy </span>
						</h2>
						<p class="text-xl mt-4 max-w-md mx-auto text-gray-400">click the next button</p>
					</div>
				</div>
			{:else if count == 1}
				<div class="flex flex-col">
					<h1
						class="text-3xl text-center p-6 font-extrabold text-black dark:text-white sm:text-4xl"
					>
						Your montly compsumation in KwH
					</h1>
					<input
						id="rounded-email"
						class=" w-96 m-auto rounded-lg border-transparent flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent"
						type="number"
						bind:value={c}
					/>
				</div>
			{:else if count == 2}
				<div class="flex flex-col">
					<h1
						class="text-3xl text-center p-6 font-extrabold text-black dark:text-white sm:text-4xl"
					>
						Your montly electricity price
					</h1>
					<input
						id="rounded-email"
						class=" w-96 m-auto rounded-lg border-transparent flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent"
						type="number"
						bind:value={p}
					/>
				</div>
			{:else if count == 3}
				<div class="flex flex-col">
					<h1
						class="text-3xl text-center p-6 font-extrabold text-black dark:text-white sm:text-4xl"
					>
						Your house rooms
					</h1>
					<select
						class="m-auto w-96 text-gray-700 py-2 px-3 border border-gray-300 bg-white rounded-md shadow-sm focus:outline-none focus:ring-primary-500 focus:border-primary-500"
						name="animals"
						bind:value={t}
					>
						<option value=""> Select an option </option>
						<option value="1 and 2 Rooms"> 1 and 2 Rooms </option>
						<option value="3 Rooms"> 3 Rooms </option>
						<option value="4 Rooms"> 4 Rooms </option>
						<option value="5 Rooms"> 5 Rooms </option>
						<option value="condominium"> Condominium </option>
					</select>
				</div>
			{:else if count == 4}
				<div class="text-center w-full mx-auto py-12 px-4 sm:px-6 lg:py-16 lg:px-8 z-20">
					<h2 class="text-3xl font-extrabold text-black dark:text-white sm:text-4xl">
						Click submit
					</h2>
				</div>
			{/if}
		</article>
		<div class="flex m-4">
			{#if count < 4}
				<button
					class="m-auto w-64 py-2 px-4  bg-indigo-600 hover:bg-indigo-700 focus:ring-indigo-500 focus:ring-offset-indigo-200 text-white w-full transition ease-in duration-200 text-center text-base font-semibold shadow-md focus:outline-none focus:ring-2 focus:ring-offset-2  rounded-lg "
					on:click={incrementCount}
					>Next
				</button>
			{:else if count == 4}
				<button
					on:click={handleSubmit}
					class="py-2 px-4  bg-indigo-600 hover:bg-indigo-700 focus:ring-indigo-500 focus:ring-offset-indigo-200 text-white w-full transition ease-in duration-200 text-center text-base font-semibold shadow-md focus:outline-none focus:ring-2 focus:ring-offset-2  rounded-lg "
					>Submit
				</button>
			{/if}
		</div>
	</div>
</section>
