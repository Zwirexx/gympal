<script lang="ts">
	import img_fitnessapp from '$lib/assets/undraw_fitness_tracker_3033.svg';
	import img_easytracking from '$lib/assets/easytracking.webp';
	import img_progress from '$lib/assets/progress.webp';
	import img_joinourcommunity from '$lib/assets/joinourcommunity.webp';
	function joinNow() {
        console.log('Join Now');
    }
</script>

<header class="h-[80svh] lg:h-[90svh] flex justify-center px-10">
    <div class="lg:grid lg:grid-cols-2 gap-4 items-center justify-items-center py-[25svh] lg:translate-x-24">
        <div class="flex space-y-8 flex-col">
            <h1 class="text-6xl font-bold">THINK LESS<br />GET STRONG</h1>
            <p class="text-lg text-surface-300 max-w-[70ch]">
                Transform your fitness journey with our app. Monitor progress, set goals, and conquer
                milestones effortlessly for a healthier, stronger you.
            </p>
            <div>
                <button class="btn variant-filled-primary" on:click={joinNow}>Join Now</button>
            </div>
        </div>
        <div class="hidden lg:block">
            <img src={img_fitnessapp} alt="Fitness App Illustration" class="max-h-96" id="fitnessapp" />
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
				<h1 class="block text-white text-2xl font-semibold">
					The easy way to track your workouts.
				</h1>
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
			<h1 class="block">MEASURE YOUR PROGRESS</h1>
		</div>
	</div>
	<div class="flex justify-center">
		<div class="pt-20 flex max-w-[1400px] flex-col-reverse xl:flex-row items-center">
			<div class="mt-12 md:mt-0 md:mr-12 flex justify-center flex-col">
				<span class="block text-white text-2xl font-semibold">See your progress unfold!</span>
				<span class="block text-[#b5b5b5] text-xl mt-2"
					>Our app gives you a clear view of your weightlifting journey. Track your lifts over time,
					watch your strength grow, and celebrate your achievements.
				</span>
			</div>
			<img loading="lazy" src={img_progress} alt="" class="md:max-h-80 w-fit" />
		</div>
	</div>
</section>
<section class="px-10 pb-11 md:px-32 md:pb-28">
	<div class="flex justify-center">
		<div class="text-white text-6xl font-bold">
			<h1 class="block">JOIN OUR COMMUNITY</h1>
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

<style>
	#fitnessapp {
		animation: float 6s ease-in-out infinite;
	}

	@keyframes float {
		0% {
			transform: translateY(0px);
		}
		50% {
			transform: translateY(-10px);
		}
		100% {
			transform: translateY(0px);
		}
	}
</style>
