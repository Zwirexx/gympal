<script>
	import FitnessApp from '$lib/assets/undraw_fitness_tracker_3033.svg';
	import img_easytracking from '$lib/assets/easytracking.png';
	import img_progress from '$lib/assets/progress.png';
	import img_joinourcommunity from '$lib/assets/joinourcommunity.png';
</script>

<main>
	<header class="h-[80svh] lg:h-[90svh] flex align-center px-10">
		<div
			class="lg:grid lg:grid-cols-2 gap-4 items-center justify-items-center py-[25svh] lg:translate-x-24"
		>
			<div class="flex space-y-8 flex-col">
				<h1 class="text-6xl">THINK LESS<br />GET STRONG</h1>
				<p class="text-lg text-surface-300 max-w-[70ch]">
					Transform your fitness journey with our app. Monitor progress, set goals, and conquer
					milestones effortlessly for a healthier, stronger you.
				</p>
				<div>
					<button class="btn variant-filled-primary">Join Now</button>
				</div>
			</div>
			<div class="hidden lg:block">
				<img src={FitnessApp} alt="" class="max-h-96" />
			</div>
		</div>
	</header>
	<section class="px-10 pb-11 md:px-32 md:pb-28">
		<div class="flex justify-center">
			<div class="text-white text-6xl font-bold mt-20">
				<span class="block">TRACK YOUR WORKOUTS</span>
			</div>
		</div>
		<div class="flex justify-center">
			<div class="pt-20 flex xl:max-w-[1400px] flex-col xl:flex-row items-center">
				<img loading="lazy" src={img_easytracking} alt="" class="md:max-h-80 w-fit" />
				<div class="mt-12 md:mt-0 md:ml-12 flex justify-center flex-col">
					<span class="block text-white text-2xl font-semibold"
						>The easy way to track your workouts.</span
					>
					<span class="block text-[#b5b5b5] text-xl mt-2"
						>No more math headaches - our built-in calculator does the heavy lifting. Just log your
						exercises, and let us handle the rest. Easy, right? Focus on your gains, not the math.
					</span>
				</div>
			</div>
		</div>
	</section>
	<section class=" px-10 pb-11 md:px-32 md:pb-28">
		<div class="flex justify-center">
			<div class="text-white text-6xl font-bold">
				<span class="block">MEASURE YOUR PROGRESS</span>
			</div>
		</div>
		<div class="flex justify-center">
			<div class="pt-20 flex max-w-[1400px] flex-col-reverse xl:flex-row items-center">
				<div class="mt-12 md:mt-0 md:mr-12 flex justify-center flex-col">
					<span class="block text-white text-2xl font-semibold">See your progress unfold!</span>
					<span class="block text-[#b5b5b5] text-xl mt-2"
						>Our app gives you a clear view of your weightlifting journey. Track your lifts over
						time, watch your strength grow, and celebrate your achievements.
					</span>
				</div>
				<img loading="lazy" src={img_progress} alt="" class="md:max-h-80 w-fit" />
			</div>
		</div>
	</section>
	<section class="px-10 pb-11 md:px-32 md:pb-28">
		<div class="flex justify-center">
			<div class="text-white text-6xl font-bold">
				<span class="block">JOIN OUR COMMUNITY</span>
			</div>
		</div>
		<div class="flex justify-center">
			<div class="pt-20 flex max-w-[1400px] flex-col xl:flex-row items-center">
				<img loading="lazy" src={img_joinourcommunity} alt="" class="md:max-h-80 w-fit" />
				<div class="mt-12 md:mt-0 md:ml-12 flex justify-center flex-col">
					<span class="block text-white text-2xl font-semibold">Be a part of something great!</span>
					<span class="block text-[#b5b5b5] text-xl mt-2"
						>Connect with like-minded individuals, share your journey, and get inspired. Together,
						we're building a supportive space for all fitness enthusiasts. Join us and let's achieve
						our goals together!
					</span>
				</div>
			</div>
		</div>
	</section>
</main>
