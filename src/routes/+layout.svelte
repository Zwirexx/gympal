<script>
	import { onMount } from 'svelte';
	import { initializeStores, Drawer, getDrawerStore } from '@skeletonlabs/skeleton';
	import { Modal, getModalStore } from '@skeletonlabs/skeleton';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
	import Icon from '@iconify/svelte';
	import Navigation from '$lib/components/Navigation.svelte';
	import PageLoader from '$lib/components/PageLoader.svelte';

	import '../app.postcss';
	import Logo from '$lib/assets/Logo.svg';

	initializeStores();

	const drawerSettings = {
		position: 'right',
		bgBackdrop: 'bg-surface-900 bg-opacity-80',
		width: 'w-2/3'
	};

	const drawerStore = getDrawerStore();

	function drawerOpen() {
		drawerStore.open(drawerSettings);
	}
</script>

<PageLoader></PageLoader>
<Modal />
<Drawer><Navigation /></Drawer>
<AppShell scrollbarGutter="auto">
	<svelte:fragment slot="header">
		<AppBar>
			<svelte:fragment slot="lead">
				<a href="/">
					<img src={Logo} alt="" class="btn" />
				</a>
			</svelte:fragment>
			<div class="hidden lg:block">
				<a href="/" class="btn hover:variant-soft-primary"> Home </a>
				<a href="/about" class="btn hover:variant-soft-primary"> About Us </a>
				<a href="/pricing" class="btn hover:variant-soft-primary"> Pricing </a>
				<a href="/blog" class="btn hover:variant-soft-primary"> Blog </a>
			</div>

			<svelte:fragment slot="trail">
				<div class="hidden lg:block">
					<a href="/login" class="btn hover:variant-soft-primary">Log in</a>
					<a href="/register" class="btn variant-filled-tertiary">Create account</a>
				</div>

				<div class="block lg:hidden">
					<button class="btn-icon hover:variant-soft-primary" on:click={drawerOpen}>
						<Icon icon="ri:menu-line" color="white" width="2rem" height="2rem" />
					</button>
				</div>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>

	<slot />
	<svelte:fragment slot="pageFooter">
		<div class="text-white">
			<div class="flex justify-center bg-surface-900 py-12">
				<a href="/" class="btn-icon btn-icon-lg hover:variant-soft-primary">
					<Icon icon="ri:instagram-line" color="white" width="2.5rem" height="2.5rem" />
				</a>
				<a href="/" class="btn-icon btn-icon-lg hover:variant-soft-primary">
					<Icon icon="ri:facebook-circle-line" color="white" width="2.5rem" height="2.5rem" />
				</a>
				<a href="/" class="btn-icon btn-icon-lg hover:variant-soft-primary">
					<Icon icon="ri:twitter-x-fill" color="white" width="2.5rem" height="2.5rem" />
				</a>
				<a
					href="https://github.com/Zwirexx"
					target="_blank"
					class="btn-icon btn-icon-lg hover:variant-soft-primary"
				>
					<Icon icon="ri:github-line" color="white" width="2.5rem" height="2.5rem" />
				</a>
			</div>
			<div class="bg-surface-900 px-32 py-8 text-center">Created by Zwirexx</div>
		</div>
	</svelte:fragment>
</AppShell>
