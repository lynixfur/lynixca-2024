<script>
	import Navbar from "$lib/Navbar.svelte";
	import "../app.css";
</script>
  
<div class="text-white" style="background:url(/sylva-in-winter.png);background-position:center;background-size:cover;">
	<div class="min-h-screen bg-gray-950 bg-opacity-70">
        <Navbar/>
		<slot />
	</div>
</div>