<script>
	import Icon from '@iconify/svelte';
	import { slide } from 'svelte/transition';
	import { fade } from 'svelte/transition';
	import { quintOut } from 'svelte/easing';

	export let menuOpen;
</script>

{#if menuOpen}
	<div
		transition:fade={{ duration: 100, easing: quintOut }}
		id="overlay"
		class="fixed w-screen h-screen z-50 bg-black bg-opacity-60 backdrop-blur-sm"
	></div>
	<nav
		transition:slide={{ duration: 300, easing: quintOut, axis: 'x' }}
		class="bg-[#222222] fixed h-screen right-0 w-3/4 z-50 shadow-2xl shadow-black px-10 py-10 border-l border-[#454545]"
	>
		<div class="flex h-screen z-10 flex-col ml-10">
			<div class="flex justify-end w-full mb-16">
				<button
					on:click={() => {
						menuOpen = false;
					}}
				>
					<Icon icon="ri:close-line" color="#F2FD84" width="4rem" height="4rem" />
				</button>
			</div>
			<div class="flex flex-col nunito text-2xl text-[#b5b5b5] h-1/3 justify-around">
				<a
					class=""
					href="/"
					on:click={() => {
						menuOpen = false;
					}}
					>Home
				</a>
				<a
					class=""
					href="/"
					on:click={() => {
						menuOpen = false;
					}}
					>About Us
				</a>
				<a
					class=""
					href="/pricing"
					on:click={() => {
						menuOpen = false;
					}}
					>Pricing
				</a>
				<a
					class=""
					href="/"
					on:click={() => {
						menuOpen = false;
					}}
					>Blog
				</a>
				<div class="nunito-sans font-bold text-xl text-white block">
					<button
						type="button"
						class="py-3 px-8 border-2 bg-white bg-opacity-0 hover:bg-opacity-10 transition-all duration-200"
						on:click={() => {
							menuOpen = false;
						}}
						>Sign Up
					</button>
					<button
						type="button"
						class="py-3 px-8"
						on:click={() => {
							menuOpen = false;
						}}
						>Log In
					</button>
				</div>
			</div>
		</div>
	</nav>
{/if}
