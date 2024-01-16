<script>
	import Banner from "$lib/Banner.svelte";
	import Navbar from "$lib/Navbar.svelte";
</script>
<main class="flex justify-center py-10">
	<div class="background-container">
		<div class="background"></div>
	</div>
	<div class="w-3/4 z-50">
		<Navbar />
		<div class="bg-cyan-900 py-2 px-5 max-w-[800px] rounded-full font-semibold -ml-1">
			Lynix is going to toronto! Make sure to reserve your stickers for the Cybersecurity Meetup!
		</div>
		<div class="grid gap-4 grid-cols-1 md:grid-cols-3">
			<div class="my-16 flex flex-col items-start grow md:col-span-2">
				<div class="flex items-center mb-5 space-x-3">
					<img src="lynix2.png" class="w-20 mb-1.5" alt="lynix"/>
					<h1 class="text-6xl font-semibold text-neutral-100">
						Hi, I'm Lynix!
					</h1>
				</div>
				<h2 class="text-3xl text-neutral-300">
					Cybersecurity Student
				</h2>
				<p class="pt-4 text-lg grow text-neutral-400">
					I'm a 20 year old VR enthusiast, Developer, Cybersecurity Student, and Furry, I'm seeking opportunities to
					change the world for better for everyone with IT.
					<br/><br/>
					<span class="text-sm text-cyan-600">Infrastructure Operational</span>
				</p>
				<div class="grid gap-5 grid-cols-5 mt-8">
					<a href="https://discord.com" aria-label="Discord">
						<i class="fa-brands fa-discord text-4xl text-neutral-400" />
					</a>
					<a href="https://t.me/cyberlynix" aria-label="Telegram">
						<i class="fa-brands fa-telegram text-4xl text-neutral-400" />
					</a>
					<a href="https://github.com/cyberlynix" aria-label="GitHub">
						<i class="fa-brands fa-github text-4xl text-neutral-400" />
					</a>
					<a href="https://twitter.com/cyberlynix" aria-label="Twitter">
						<i class="fa-brands fa-twitter text-4xl text-neutral-400" />
					</a>
					<a href="https://www.linkedin.com/in/anthony-roy-6316a624b/" aria-label="LinkedIn">
						<i class="fa-brands fa-linkedin text-4xl text-neutral-400" />
					</a>
				</div>
			</div>
		</div>
	</div>
</main>