<script lang="ts">
	let isOpen = false;
	const toggleNav = () => {
		isOpen = !isOpen;
	};
</script>

<header class=" text-white items-center py-14 md:flex hidden">
	<nav class="flex items-center space-x-8">
		<a href="/" class="font-semibold text-lg">
			<img src="/lynix.png" alt="lynix" class="h-10 w-10 mb-1.5" />
		</a>
		<a href="/projects" class="font-semibold text-lg hover:text-cyan-600 transition-colors">Projects</a>
		<a href="/blog" class="font-semibold text-lg hover:text-cyan-600 transition-colors">Blog</a>
		<a href="/events" class="font-semibold text-lg hover:text-cyan-600 transition-colors flex items-center">Events
			<i class="fa fa-circle text-xs ml-2 text-cyan-700 animate-pulse" aria-hidden="true"></i>
		</a>
		<a href="/about" class="font-semibold text-lg hover:text-cyan-600 transition-colors">About</a>
		<a href="/contact" class="font-semibold text-lg hover:text-cyan-600 transition-colors">Contact</a>
	</nav>
	<!-- TODO: Work on mobile interface -->
	<button class="nav-button hidden" on:click={toggleNav} aria-label="Toggle Navigation">
        <svg height="24px" width="24px" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 1h15M1 7h15M1 13h15"/>
        </svg>
	</button>
</header>