<script lang="ts">
	import { Client, Account, ID } from 'appwrite';
	const client = new Client();
	client.setEndpoint('https://cloud.appwrite.io/v1').setProject('649ae9651ccb6065b211');
	const account = new Account(client);

	function handleGoogle() {
		account.createOAuth2Session('google', 'https://blog-hack.vercel.app/');
	}
	function handleGithub() {
		account.createOAuth2Session('github');
	}
</script>

<section class="flex justify-center h-[580px] items-center">
	<div class="text-center h-[400px] w-[350px] rounded-md shadow-lg bg-slate-50 p-4">
		<h1 class="text-xl text-black font-medium">Sign In</h1>
		<div class="mt-6 flex flex-col gap-3">
			<button
				class="bg-gray-400 px-2 py-1 rounded-md text-white font-medium hover:bg-gray-200 hover:text-black"
				on:click={handleGoogle}>Sign In with Google</button
			>
			<button
				on:click={handleGithub}
				class="bg-gray-400 px-2 py-1 rounded-md text-white font-medium hover:bg-gray-200 hover:text-black"
				>Sign In with Github</button
			>
		</div>
	</div>
</section>
