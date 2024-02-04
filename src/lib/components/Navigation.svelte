<script lang="ts">
	import { getDrawerStore } from '@skeletonlabs/skeleton';
	import Icon from '@iconify/svelte';
	const drawerStore = getDrawerStore();

	function drawerClose() {
		drawerStore.close();
	}
</script>

<nav class="list-nav p-14 space-y-4">
	<div class="flex">
		<button class="btn hover:variant-soft-primary" on:click={drawerClose}>
			<Icon icon="ri:arrow-left-line" color="white" width="2rem" height="2rem" />
		</button>
	</div>

	<ul>
		<li>
			<a href="/" class="btn hover:variant-soft-primary" on:click={drawerClose}> Home </a>
		</li>
	</ul>
	<ul>
		<li>
			<a href="/about" class="btn hover:variant-soft-primary" on:click={drawerClose}> About Us </a>
		</li>
	</ul>

	<ul>
		<li>
			<a href="/pricing" class="btn hover:variant-soft-primary" on:click={drawerClose}> Pricing </a>
		</li>
	</ul>
	<ul>
		<li>
			<a href="/blog" class="btn hover:variant-soft-primary" on:click={drawerClose}> Blog </a>
		</li>
	</ul>
	<ul class="pt-4">
		<li>
			<a href="/login" class="btn hover:variant-soft-primary" on:click={drawerClose}>Log In</a>
		</li>
	</ul>
	<ul>
		<li>
			<a href="/register" class="btn variant-filled-tertiary" on:click={drawerClose}
				>Create account</a
			>
		</li>
	</ul>
</nav>
