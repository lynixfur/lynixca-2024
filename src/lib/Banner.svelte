<script>
	import { onMount } from "svelte";
	// @ts-ignore
	import { fade, blur, fly, slide, scale } from "svelte/transition";
	// @ts-ignore
	import { quintOut } from "svelte/easing";

	let welcome = "Bonjour!";

	const words = [
		"Authentik",
		"Terraform",
		"Grafana",
		"JavaScript",
		"TypeScript",
		"MySQL",
		"NestJS",
		"NodeJS",
		"PostgreSQL",
		"TailwindCSS",
		"Redis",
		"Svelte",
		"SvelteKit",
		"Python",
		"Vue",
		"NGINX",
		"Docker",
		"REST",
		"TypeORM",
		"Express",
		"Linux",
		"Composer",
		"JSX",
		"Backblaze"
	];

	const welcomes = [
		"Bonjour!",
		"Hey!",
		"Hewwo~",
		"Salut!",
		"OwO",
		"Hello!",
		"B.O.O.P!"
	];

	// @ts-ignore
	function calculateAge(birthday) { // birthday is a date
		var ageDifMs = Date.now() - birthday;
		var ageDate = new Date(ageDifMs); // miliseconds from epoch
		return Math.abs(ageDate.getUTCFullYear() - 1970);
	}

	onMount(() => {
		for(let j = 0; j < 20; j++) {
			let list = document.createElement('div');
			list.classList.add('flex', "gap-2");

			for (let i = 0; i < 20; i++) {
				const word = words[Math.floor(Math.random() * words.length)];
				let element = document.createElement('span');
				element.innerHTML = word;
				element.classList.add("text-9xl", "p-10", "whitespace-nowrap");

				list.appendChild(element);
			}

			// @ts-ignore
			document.getElementById('lists').appendChild(list);
		}

		let i = 0;
		setInterval(() => {
			welcome = welcomes[i % 7];
			i++;
		}, 3000);
	});
</script>

<main class="relative overflow-hidden min-h-screen @container">
	<div class="absolute inset-0 w-full h-screen flex flex-col items-center gap-1 justify-center font-bold anim opacity-5 dark:opacity-5" id="lists">
	</div>

	<div class="flex justify-center items-center h-screen">
		<div class="flex space-x-10">
			<img src={"/lynix.png"} alt="Lynix" class="w-[30vw] z-10"/>
			<div class="flex flex-col gap-10">
				<h1 class="text-5xl font-bold italic text-cyan-500">{#key welcome}<span in:scale>{welcome}</span>{/key}</h1>

				<span class="flex gap-2 flex-wrap items-end">
					<h2 class="text-4xl flex gap-2 font-extrabold">I'm
						<span class="flex items-center">
							Lynix
							<h2 class="text-4xl font-extrabold">,</h2>
						</span>
					</h2>
					<span class="text-4xl font-extralight">
						your canadian IT Specalist. 🍁
					</span>
				</span>

				<p class="text-gray-300 lg:text-lg max-w-[800px]">
					I'm a {calculateAge(new Date("2003-12-09"))} year old VR enthusiast, Developer, Cybersecurity Student, and Furry, I'm seeking opportunities to
					change the world for better for everyone with IT.
	
					<br /><br />
					I'm currently working on a few projects, including <span class="text-cyan-500">Furality</span>, a few websites commissions, and a few other personal projects.
					<br /><br />
					I work with a variety of technologies, including but not limited to:
					NestJs, NextJS, NuxtJS, Svelte, SvelteKit, TypeScript, JavaScript, Vue, Python, and more.
	
				</p>
				
				<div>
					<p class="text-2xl font-extrabold text-green-500">Website Opening Soon, Jan 1st 2024!</p>
					<p class="txt-small text-gray-400 font-semibold">Backdrop Animation by: Midblep </p>
				</div>
			</div>
		</div>
	</div>
</main>

<style>
	.anim {
		user-select: none;
		animation: anim;
		animation-duration: 200s;
		animation-timing-function: linear;
		animation-iteration-count: infinite;
	}

	@keyframes anim {
		0% {
			transform: translate(-100%,100%) rotate(-30deg);
		}
		100% {
			transform: translate(100%,-100%) rotate(-30deg);
		}
	}
	.popout {
		animation: popout;
		animation-duration: 1s;
		animation-timing-function: ease-in-out;
	}

	@keyframes popout {
		0% {
			transform: scale(1) rotate(0deg);
		}
		50% {
			transform: scale(1.2) rotate(-5deg);
		}
		100% {
			transform: scale(1) rotate(0deg);
		}
	}

	@keyframes float {
		0% {
			padding-top: 0px;
			padding-bottom: 10px;
		}
		50% {
			padding-top: 10px;
			padding-bottom: 0px;
		}
		100% {
			padding-top: 0px;
			padding-bottom: 10px;
		}
	}

	.float {
		animation: float;
		animation-duration: 2s;
		animation-iteration-count: infinite;
		animation-timing-function: ease-in-out;
	}

	@keyframes float {
		0% {
			padding-top: 0px;
			padding-bottom: 30px;
		}
		50% {
			padding-top: 10px;
			padding-bottom: 20px;
		}
		100% {
			padding-top: 0px;
			padding-bottom: 30px;
		}
	}

	/* Lynix */

	@keyframes float {
		0%,
		100% {
			transform: translateY(-5px);
		}

		50% {
			transform: translateY(-15px);
		}
	}

	.float-animation {
		animation: float 3s ease-in-out infinite;
	}
</style>