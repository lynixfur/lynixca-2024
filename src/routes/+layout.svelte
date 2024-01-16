<script>
	import Navbar from "$lib/Navbar.svelte";
	import Banner from "$lib/Banner.svelte"; 
	import "../app.css";

	import { page } from '$app/stores';  
</script>
  
<div class="text-white">
	<div class="min-h-screen flex justify-center">
		{#if $page.url?.pathname == "/"}
		<div class="background-container">
		  	<div class="background"></div>

		  	<!-- CN Tower -->
			<p class="hidden">CN Tower by Fatemah Manji from https://thenounproject.com/browse/icons/term/cn-tower/ (CC BY 3.0)</p>
			<img src="/cn-tower.svg" class="z-20 fixed bottom-0 right-10 w-[700px]" alt="Toronto CN Tower"/>
		</div>
	  	{/if}
		<div class="z-50 w-3/4 ">
			<Navbar />
			<Banner />
			<slot />
		</div>
	</div>
</div>