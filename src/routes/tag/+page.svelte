<script lang="ts">
	let search = '';
	let testArray = [
		'#react',
		'#svelte',
		'#weddevelopment',
		'#dev_danny',
		'#nacos',
		'#react',
		'#svelte',
		'#weddevelmkwdsnxopment',
		'#dev_danny',
		'#nacos',
		'#react',
		'#sverlwmsnlte',
		'#wedderwdsvelopment',
		'#dev_danny',
		'#nacos',
		'#react',
		'#svelte',
		'#weddevelopment',
		'#dev_danny',
		'#nacos',
		'#react',
		'#svelte',
		'#weddevelopment',
		'#dev_danny',
		'#nacos'
	];

	function handleSearch() {
		console.log('r3wjhdsg');
	}
</script>

<section class="grid place-content-center">
	<div class="md:mt-24 mt-36">
		<form class="relative w-[520px] md:w-[550px] md:mx-auto mx-4">
			<input
				class="px-3 pr-10 py-2 focus:outline-blue-300 border-2 w-full border-black rounded-3xl text-lg"
				type="text"
				bind:value={search}
				required
				placeholder="Find the topis you care about..."
			/>
			<button
				on:click={handleSearch}
				class="absolute top-3 right-3 w-[26px] h-[26px] text-xl cursor-pointer"
				><svg
					xmlns="http://www.w3.org/2000/svg"
					fill="none"
					viewBox="0 0 24 24"
					stroke-width="1.5"
					stroke="currentColor"
					class="w-6 h-6"
				>
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z"
					/>
				</svg></button
			>
		</form>
		<div class="mt-12 md:w-[750px] w-[545px] flex flex-wrap gap-3">
			{#each testArray as item}
				<button class="w-fit text-center text-black font-medium bg-slate-200 rounded-3xl px-3 py-2"
					>{item}</button
				>
			{/each}
		</div>
	</div>
</section>
