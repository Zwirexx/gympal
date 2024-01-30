<script>
	import Icon from '@iconify/svelte';
</script>

<div class="w-screen h-full justify-center flex items-center p-8 md:p-20">
	<form
		action="/register"
		method="post"
		class="p-12 w-full md:max-w-fit space-y-6 variant-glass-surface border-surface-600 border rounded-lg"
	>
		<h1 class="text-4xl">Register</h1>
		<label class="label min-w-full md:min-w-[60ch]">
			<span>Username</span>
			<input class="input" name="username" type="text" placeholder="Type in your username" />
		</label>
		<label class="label min-w-full md:min-w-[60ch]">
			<span>Email</span>
			<input class="input" name="email" type="email" placeholder="Type in your email" />
		</label>
		<label class="label min-w-full md:min-w-[60ch]">
			<span>Password</span>
			<input class="input" name="password" type="password" placeholder="Type in your password" />
		</label>

		<button class="btn variant-filled-primary">Create account</button>
		<hr />
		<div class="flex justify-center items-center flex-col md:flex-row space-y-4 md:space-y-0">
			<button class="btn variant-ghost-surface space-x-4">
				<Icon icon="akar-icons:github-fill" color="#fff" width="2rem" height="2rem" />
				<span>Continue with GitHub</span>
			</button>
			<div class="divider-vertical h-8 hidden md:block" />
			<hr class="md:w-0 w-32" />
			<button class="btn variant-ghost-surface space-x-4">
				<Icon icon="akar-icons:google-fill" color="#fff" width="2rem" height="2rem" />
				<span>Continue with Google</span>
			</button>
		</div>
	</form>
</div>
