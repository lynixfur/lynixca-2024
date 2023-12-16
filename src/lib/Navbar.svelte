<script lang="ts">
	let isOpen = false;
	const toggleNav = () => {
		isOpen = !isOpen;
	};
</script>

<header class="bg-darker border-b border-card shadow-md text-white p-3 flex items-center space-x-10 px-10 py-3">
	<a href="/"><h1 style="text-shadow: 5px 5px #075985;" class="flex items-center text-4xl font-semibold font-cyber tracking-widest text-cyan-400 uppercase rounded-lg focus:outline-none focus:shadow-outline">LYNIX.CA</h1></a>
	<nav class="flex itemsc-enter space-x-5">
		<a href="/projects" class="font-semibold text-lg">Projects</a>
		<a href="/blog" class="font-semibold text-lg">Blog</a>
		<a href="/fursona" class="font-semibold text-lg">Fursona</a>
		<a href="/about" class="font-semibold text-lg">About</a>
		<a href="/contact" class="font-semibold text-lg">Contact</a>
	</nav>
	<!-- TODO: Work on mobile interface -->
	<button class="nav-button hidden" on:click={toggleNav} aria-label="Toggle Navigation">
        <svg height="24px" width="24px" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 1h15M1 7h15M1 13h15"/>
        </svg>
	</button>
</header>