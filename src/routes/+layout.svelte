<script>
	import '../app.css';
	import PageLoader from './PageLoader.svelte';
	import Icon from '@iconify/svelte';
</script>

<PageLoader />
<nav class="bg-[#222222] px-32 pt-11">
	<div class="relative flex items-center z-10">
		<div>
			<a href="/">
				<img src="src/assets/Logo@4x.jpg" alt="" class="h-10" />
			</a>
		</div>
		<div class="nunito text-xl text-[#b5b5b5] ml-28">
			<a class="mr-16" href="/">Home</a>
			<a class="mr-16" href="/">About Us</a>
			<a class="mr-16" href="/pricing">Pricing</a>
			<a class="mr-16" href="/">Blog</a>
		</div>
		<div class="nunito-sans font-bold text-xl text-white ml-auto">
			<button
				type="button"
				class="py-3 px-8 border-2 bg-white bg-opacity-0 hover:bg-opacity-10 transition-all duration-200"
				>Sign Up</button
			>
			<button type="button" class="py-3 px-8">Log In</button>
		</div>
	</div>
</nav>

<slot />

<footer class="text-white">
	<div class="bg-[#181818] px-32 py-16 flex justify-center">
		<div class="w-1/3 flex justify-between">
			<a href="/"><Icon icon="ri:instagram-line" color="#F2FD84" width="48" height="48" /> </a>
			<a href="/"
				><Icon icon="ri:facebook-circle-line" color="#F2FD84" width="48" height="48" />
			</a>
			<a href="/"><Icon icon="ri:twitter-x-fill" color="#F2FD84" width="48" height="48" /> </a>
			<a href="https://github.com/Zwirexx" target="_blank">
				<Icon icon="ri:github-line" color="#F2FD84" width="48" height="48" />
			</a>
		</div>
	</div>
	<div class="bg-[#111111] px-32 py-8 text-center">Created by Zwirexx</div>
</footer>
