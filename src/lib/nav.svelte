<script>
	import { headerLogo } from '../assets/images';
	import { hamburger } from '../assets/icons';
	import { navLinks } from '../constants';

	import { onMount } from 'svelte';
  

	let isMobile = false;
	let isMobileMenuOpen = false;

	onMount(() => {
		// Check window width when the component is mounted on the client
		isMobile = window.innerWidth < 768;

		// Update isMobile when window is resized
		window.addEventListener('resize', () => {
			isMobile = window.innerWidth < 768;
		});
	});

	function toggleMobileMenu() {
		isMobileMenuOpen = !isMobileMenuOpen;
	}
</script>

<header class="padding-x py-4 {isMobile ? '' : 'absolute'} w-full z-10">

  <div>
    <button class="hidden max-lg:block" on:click={toggleMobileMenu}>
      <img src={hamburger} alt="hamburger" width={25} height={25} />
    </button>
  </div>

	<nav class="flex justify-between items-center max-container">
		{#if isMobile}
			<ul
				class="flex-col bg-white md:w-auto w-full left-0 py-4 md:pl-0 pl-4 {isMobileMenuOpen ? '' : 'hidden'}"
			>
				{#each navLinks as link}
					<li class="my-3 md:my-0 hover:bg-gray-100 rounded-md px-3 py-2">
						<a href={link.href} class="font-montserrat leading-normal text-lg text-slate-gray">{link.label}</a>
					</li>
				{/each}
			</ul>
		{:else}
			<ul class="flex-1 flex justify-center items-center gap-16 max-lg:hidden">
				{#each navLinks as link}
					<li class="hover:bg-gray-100 rounded-md px-3 py-2">
						<a href={link.href} class="font-montserrat leading-normal text-lg text-slate-gray">{link.label}</a>
					</li>
				{/each}
			</ul>
		{/if}
	</nav>
</header>




