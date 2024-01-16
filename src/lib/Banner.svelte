<script lang="ts">
	import { onMount } from 'svelte';
  
	let daysUntilToronto = 0;
  
	const targetDate = new Date('March 14, 2024 00:00:00').getTime();
  
	function updateCountdown() {
	  const currentDate = new Date().getTime();
	  const timeDifference = targetDate - currentDate;
	  daysUntilToronto = Math.floor(timeDifference / (1000 * 60 * 60 * 24));
	}
  
	onMount(() => {
	  // Initial update
	  updateCountdown();
  
	  // Update every second
	  const interval = setInterval(updateCountdown, 1000);
  
	  // Clear the interval on component destruction
	  return () => clearInterval(interval);
	});
  </script>
  
  {#if daysUntilToronto > 0}
  <div class="bg-cyan-900 py-2 px-5 max-w-[800px] rounded-full font-semibold -ml-1">
	  Lynix is going to Toronto in {daysUntilToronto} days! Make sure to reserve your stickers for the meetup!
  </div>
  {/if}
  