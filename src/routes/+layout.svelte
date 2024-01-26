<script>
	import '../app.css';
	import PageLoader from '$lib/PageLoader.svelte';
	import LandingPageMenu from '$lib/LandingPageMenu.svelte';
	import Icon from '@iconify/svelte';
	import img_logo from '$lib/assets/Logo.svg';

	let menuOpen = false;
</script>

<PageLoader />
<LandingPageMenu bind:menuOpen></LandingPageMenu>
<nav class="bg-[#222222] px-5 pt-11 md:px-32 md:pt-11">
	<div class="relative flex items-center z-10 flex-row">
		<div>
			<a href="/" class="">
				<img src={img_logo} alt="" class="min-h-10 max-w-fit" />
			</a>
		</div>
		<div class="hidden min-[1380px]:block nunito text-xl text-[#b5b5b5] ml-28">
			<a class="mr-16" href="/">Home</a>
			<a class="mr-16" href="/">About Us</a>
			<a class="mr-16" href="/pricing">Pricing</a>
			<a class="mr-16" href="/">Blog</a>
		</div>
		<div class="nunito-sans font-bold text-xl text-white ml-auto hidden min-[1380px]:block">
			<button
				type="button"
				class="py-3 px-8 border-2 bg-white bg-opacity-0 hover:bg-opacity-10 transition-all duration-200"
				>Sign Up</button
			>
			<button type="button" class="py-3 px-8">Log In</button>
		</div>
		<div class="flex justify-end w-full min-[1380px]:hidden">
			<button
				on:click={() => {
					menuOpen = true;
				}}
			>
				<Icon icon="ri:menu-line" color="#F2FD84" width="3rem" height="3rem" />
			</button>
		</div>
	</div>
</nav>

<slot />

<footer class="text-white">
	<div class="bg-[#181818] md:px-32 py-16 flex justify-center">
		<div class="md:w-1/3 w-1/2 flex justify-between">
			<a href="/" class="hover:opacity-75 transition-all duration-200">
				<Icon icon="ri:instagram-line" color="#F2FD84" width="3rem" height="3rem" />
			</a>
			<a href="/" class="hover:opacity-75 transition-all duration-200">
				<Icon icon="ri:facebook-circle-line" color="#F2FD84" width="3rem" height="3rem" />
			</a>
			<a href="/" class="hover:opacity-75 transition-all duration-200">
				<Icon icon="ri:twitter-x-fill" color="#F2FD84" width="3rem" height="3rem" />
			</a>
			<a
				href="https://github.com/Zwirexx"
				target="_blank"
				class="hover:opacity-75 transition-all duration-200"
			>
				<Icon icon="ri:github-line" color="#F2FD84" width="3rem" height="3rem" />
			</a>
		</div>
	</div>
	<div class="bg-[#111111] px-32 py-8 text-center">Created by Zwirexx</div>
</footer>
