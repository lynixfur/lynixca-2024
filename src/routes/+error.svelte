<script>
	import Banner from "$lib/Banner.svelte";
	import Navbar from "$lib/Navbar.svelte";
</script>
<main class="flex justify-center py-10 h-screen">
	<div class="background-container">
		<div class="background"></div>
	</div>
	<div class="w-3/4 z-50">
		<Navbar />

        <!-- 404 Page -->
        <div class="flex flex-col items-center justify-center">
            <h1 class="text-6xl font-semibold text-cyan-600">
                404
            </h1>
            <h2 class="text-3xl text-neutral-300">
                Page not found
            </h2>
            <p class="pt-4 text-lg grow text-neutral-400">
                The page you are looking for does not exist.
            </p>
	</div>
</main>