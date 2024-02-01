<script>
	import Icon from '@iconify/svelte';
	import { RadioGroup, RadioItem } from '@skeletonlabs/skeleton';

	let annually = false;
</script>

<div class="w-full flex items-center flex-col">
	<RadioGroup
		class="mt-10 mb-10"
		active="variant-filled-primary"
		hover="hover:variant-soft-primary"
	>
		<RadioItem bind:group={annually} name="pricing" value={false}>Monthly</RadioItem>
		<RadioItem bind:group={annually} name="pricing" value={true}>Annually</RadioItem>
	</RadioGroup>

	<div
		class="w-screen h-full flex flex-col space-y-12 lg:flex-row lg:space-y-0 justify-center items-center lg:space-x-10"
	>
		<!-- ZDUPLIKOWANY KOD. -->
		<!-- PRACE NAD ANIMACJĄ -->
		<!-- DO POPRAWY -->
		{#if !annually}
			<div class="card p-6 w-1/3 variant-ghost-surface h-2/3">
				<header class="card-header">
					<div class="flex space-x-12 items-center justify-center">
						<div class="flex flex-col space-y-3 w-[10ch]">
							<div
								class="text-sm border border-surface-300 rounded text-surface-300 w-fit px-3 py-1 font-medium"
							>
								FREE
							</div>
							<div class="h1 font-bold">$0</div>
							<div>Per month</div>
						</div>
						<div class=" divider-vertical h-20"></div>
						<div>
							<ul class="space-y-2">
								<li class="flex items-center space-x-3">
									<Icon icon="mdi:tick-circle" /> <span>Basic Exercise Tracking</span>
								</li>
								<li class="flex items-center space-x-3">
									<Icon icon="mdi:tick-circle" /> <span>Progress Overview</span>
								</li>
								<li class="flex items-center space-x-3">
									<Icon icon="mdi:tick-circle" /> <span>General Statistics</span>
								</li>
							</ul>
						</div>
					</div>
				</header>
				<footer class="mt-4">
					<div class="w-full text-center">
						<button class="btn variant-filled-tertiary w-2/3">Choose plan</button>
					</div>
				</footer>
			</div>

			<div class="card p-6 w-fit variant-ghost-surface h-2/3">
				<header class="card-header">
					<div class="flex space-x-12 items-center justify-center">
						<div class="flex flex-col space-y-3 w-[10ch]">
							<div
								class="text-sm border border-surface-300 rounded text-surface-300 w-fit px-3 py-1 font-medium"
							>
								PREMIUM
							</div>
							<div class="h1 font-bold">$19</div>
							<div>Per month</div>
						</div>
						<div class=" divider-vertical h-20"></div>
						<div>
							<ul class="space-y-2">
								<li class="flex items-center space-x-3">
									<Icon icon="mdi:tick-circle" /> <span>Personalized Workout Plans</span>
								</li>
								<li class="flex items-center space-x-3">
									<Icon icon="mdi:tick-circle" /> <span>Advanced Statistics and Analysis</span>
								</li>
								<li class="flex items-center space-x-3">
									<Icon icon="mdi:tick-circle" /> <span>Exclusive Training Content</span>
								</li>
							</ul>
						</div>
					</div>
				</header>
				<footer class="mt-4">
					<div class="w-full text-center">
						<button class="btn variant-filled-tertiary w-2/3">Choose plan</button>
					</div>
				</footer>
			</div>
		{:else}
			<div class="card p-6 w-1/3 variant-ghost-surface h-2/3">
				<header class="card-header">
					<div class="flex space-x-12 items-center justify-center">
						<div class="flex flex-col space-y-3 w-[10ch]">
							<div
								class="text-sm border border-surface-300 rounded text-surface-300 w-fit px-3 py-1 font-medium"
							>
								FREE
							</div>
							<div class="h1 font-bold">$0</div>
							<div>
								Per month
								<div class="text-sm text-surface-400">$0 yearly</div>
							</div>
						</div>
						<div class=" divider-vertical h-20"></div>
						<div>
							<ul class="space-y-2">
								<li class="flex items-center space-x-3">
									<Icon icon="mdi:tick-circle" /> <span>Basic Exercise Tracking</span>
								</li>
								<li class="flex items-center space-x-3">
									<Icon icon="mdi:tick-circle" /> <span>Progress Overview</span>
								</li>
								<li class="flex items-center space-x-3">
									<Icon icon="mdi:tick-circle" /> <span>General Statistics</span>
								</li>
							</ul>
						</div>
					</div>
				</header>
				<footer class="mt-4">
					<div class="w-full text-center">
						<button class="btn variant-filled-tertiary w-2/3">Choose plan</button>
					</div>
				</footer>
			</div>
			<div class="relative">
				<span
					class="badge variant-filled-warning absolute top-0 right-0 mt-[-1rem] mr-[-2rem] z-10 text-lg px-4 py-1"
					>-21% OFF</span
				>
				<div class="card p-6 w-fit variant-ghost-surface h-2/3">
					<header class="card-header">
						<div class="flex space-x-12 items-center justify-center">
							<div class="flex flex-col space-y-3 w-[10ch]">
								<div
									class="text-sm border border-surface-300 rounded text-surface-300 w-fit px-3 py-1 font-medium"
								>
									PREMIUM
								</div>

								<div class="h1 font-bold">$15</div>

								<div>
									Per month
									<div class="text-sm text-surface-400">$180 yearly</div>
								</div>
							</div>
							<div class=" divider-vertical h-20"></div>
							<div>
								<ul class="space-y-2">
									<li class="flex items-center space-x-3">
										<Icon icon="mdi:tick-circle" /> <span>Personalized Workout Plans</span>
									</li>
									<li class="flex items-center space-x-3">
										<Icon icon="mdi:tick-circle" /> <span>Advanced Statistics and Analysis</span>
									</li>
									<li class="flex items-center space-x-3">
										<Icon icon="mdi:tick-circle" /> <span>Exclusive Training Content</span>
									</li>
								</ul>
							</div>
						</div>
					</header>
					<footer class="mt-4">
						<div class="w-full text-center">
							<button class="btn variant-filled-tertiary w-2/3">Choose plan</button>
						</div>
					</footer>
				</div>
			</div>
		{/if}
	</div>
</div>
