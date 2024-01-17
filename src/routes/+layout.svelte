<script>
	import Navbar from "$lib/Navbar.svelte";
	import Banner from "$lib/Banner.svelte"; 
	import "../app.css";

	import { page } from '$app/stores';  
</script>
  
<div class="text-white">
	<div class="min-h-screen flex justify-center">
		{#if $page.url?.pathname == "/"}
		<div class="background-container w-full">
		  	<div class="background"></div>

		  	<!-- CN Tower -->
			<p class="hidden">CN Tower by Fatemah Manji from https://thenounproject.com/browse/icons/term/cn-tower/ (CC BY 3.0)</p>
			<img src="/cn-tower.svg" class="cn-tower" alt="Toronto CN Tower"/>
		</div>
	  	{/if}
		<div class="z-50 md:w-3/4 w-full md:px-0 px-7">
			<Navbar />
			<Banner />
			<slot />
		</div>
	</div>
</div>