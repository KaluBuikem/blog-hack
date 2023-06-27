<script>
	let search = '';
	let showSearch = false;

	function handleShow() {
		showSearch = !showSearch;
	}

	function handleSearch() {
		console.log(search);
	}
</script>

<header class="container mx-auto flex justify-between py-2 px-3 items-center">
	<div class="flex items-center gap-6">
		<div class="w-14 h-14">
			<img src="/favicon.png" alt="Hero" />
		</div>
		<nav>
			<ul class="flex flex-row gap-4 font-sans font-medium text-slate-700">
				<li class=" hover:underline transition-colors"><a href="/">Home</a></li>
				<li class=" hover:underline transition-colors"><a href="/tag">Tags</a></li>
			</ul>
		</nav>
	</div>
	<div class="flex gap-3 items-center">
		<form class="relative {showSearch ? '' : 'hidden'}">
			<input
				class="px-2 py-1 rounded-lg focus:outline-blue-300 border"
				type="text"
				id="password"
				required
				aria-required="true"
				bind:value={search}
			/>
			<button
				on:click={handleSearch}
				class="absolute top-1 right-3 w-[26px] h-[26px] text-xl cursor-pointer"
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
		<button
			on:click={handleShow}
			class=" w-[26px] h-[26px] text-xl cursor-pointer {showSearch ? 'hidden' : ''}"
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
		<a
			href="/login"
			class="border-2 border-black px-2 py-1 text-center rounded-xl font-sans w-[85px] block cursor-pointer hover:text-white hover:bg-black"
		>
			Login
		</a>
	</div>
</header>
