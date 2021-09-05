<script>
	import { onMount } from 'svelte';
	import auth from '$lib/authService';
	import { isAuthenticated, user } from '$lib/store';
	let auth0Client;
	onMount(async () => {
		auth0Client = await auth.createClient();
		isAuthenticated.set(await auth0Client.isAuthenticated());
		user.set(await auth0Client.getUser());
	});

	function login() {
		auth.loginWithPopup(auth0Client);
	}

	function logout() {
		auth.logout(auth0Client);
	}
	$: innerWidth = 0;
	let formText = '';
</script>

<div>
	<nav class="bg-white dark:bg-gray-800  shadow ">
		<div class="max-w-7xl mx-auto px-8">
			<div class="flex items-center justify-between h-16">
				<div class="w-full justify-between flex items-center">
					<a class="flex-shrink-0" href="/">
						<img
							class="h-8 w-8"
							src="https://cdn.discordapp.com/attachments/883374253989298176/883784525421871184/energify-logos_black.png"
							alt="Workflow"
						/>
					</a>
					<div class="md:block">
						<div class="ml-10 flex items-baseline space-x-4">
							<a
								class="text-gray-300  hover:text-gray-800 dark:hover:text-white px-3 py-2 rounded-md text-sm font-medium"
								href="/"
							>
								Home
							</a>
							<a
								class="text-gray-300  hover:text-gray-800 dark:hover:text-white px-3 py-2 rounded-md text-sm font-medium"
								href="/add"
							>
								Contact
							</a>
							{#if $isAuthenticated}
								<a
									class="text-gray-300 hover:text-gray-800 dark:hover:text-white block px-3 py-2 rounded-md text-base font-medium"
									on:click={logout}>Logout</a
								>
							{:else}
								<a
									class="text-gray-300 hover:text-gray-800 dark:hover:text-white block px-3 py-2 rounded-md text-base font-medium"
									on:click={login}>Login</a
								>
							{/if}
						</div>
					</div>
				</div>
			</div>
		</div>
	</nav>
</div>
