<script>
	import img_jackedguy from '$lib/assets/jacked-guy-bg.jpg';
	import img_easytracking from '$lib/assets/easytracking.png';
	import img_progress from '$lib/assets/progress.png';
	import img_joinourcommunity from '$lib/assets/joinourcommunity.png';
	import img_stripes from '$lib/assets/bg.png';
</script>

<div class="absolute xl:hidden top-0 right-0 z-0 gradient-yellow w-screen h-screen"></div>
<title>Meet GymPal</title>
<section class="bg-[#222222] max-h-screen px-10 py-32 md:px-32 md:py-32 z-10">
	<img src={img_jackedguy} alt="" class="hidden xl:block absolute top-0 right-0 h-full z-0" />
	<div class="relative z-10">
		<div class="lg:max-w-[60%]">
			<div class="text-white text-7xl hakuna-sans font-bold">
				<span class="block">THINK LESS</span>
				<span class="block">GET STRONG</span>
			</div>
			<div>
				<span class="block text-[#b5b5b5] text-xl nunito mt-6 md:mt-12"
					>Transform your fitness journey with our app. Monitor progress, set goals, and conquer
					milestones effortlessly for a healthier, stronger you.
				</span>
			</div>
			<a
				href="https://youtu.be/gkjSXBCVo8E"
				target="_blank"
				type="button"
				class="py-3 px-8 bg-[#F2FD84] max-w-56 text-xl font-bold nutino-sans mt-12 hover:bg-opacity-85 transition-all duration-200"
				>JOIN NOW
			</a>
		</div>
	</div>
</section>
<section class="bg-[#222222] max-h-screen px-10 pb-11 md:px-32 md:pb-11 z-10">
	<div
		class="flex flex-col md:flex-row glass w-full mb-0 mt-auto py-10 px-12 text-white items-center text-lg"
	>
		<div class="flex flex-col md:flex-row md:justify-evenly md:w-full">
			<div class="mb-16 md:mb-0 md:mr-6">
				<span class="block hakuna-sans text-5xl">100K</span>
				<span class="block nunito font-bold">Active users</span>
				<span class="block nunito text-[#b5b5b5]">Our community is growing fast!</span>
			</div>
			<div class="mb-16 md:mb-0 md:mr-6">
				<span class="block hakuna-sans text-5xl">10</span>
				<span class="block nunito font-bold">Free routines</span>
				<span class="block nunito text-[#b5b5b5]">Pick from various workout plans.</span>
			</div>
			<div>
				<span class="block hakuna-sans text-5xl">99%</span>
				<span class="block nunito font-bold">Happy Customers</span>
				<span class="block nunito text-[#b5b5b5]">Nearly everyone loves our app!</span>
			</div>
		</div>
	</div>
</section>

<main
	class="bg-[#222222] bg-no-repeat bg-center bg-cover z-10"
	style="background-image: url({img_stripes});"
>
	<section class="px-10 pb-11 md:px-32 md:pb-28">
		<div class="flex justify-center">
			<div class="text-white text-6xl hakuna-sans font-bold mt-20">
				<span class="block">TRACK YOUR WORKOUTS</span>
			</div>
		</div>
		<div class="flex justify-center">
			<div class="pt-20 flex xl:max-w-[1400px] flex-col xl:flex-row items-center">
				<img loading="lazy" src={img_easytracking} alt="" class="md:max-h-80 w-fit" />
				<div class="mt-12 md:mt-0 md:ml-12 flex justify-center flex-col">
					<span class="block text-white text-2xl nunito">The easy way to track your workouts.</span>
					<span class="block text-[#b5b5b5] text-xl nunito mt-2"
						>No more math headaches - our built-in calculator does the heavy lifting. Just log your
						exercises, and let us handle the rest. Easy, right? Focus on your gains, not the math.
					</span>
				</div>
			</div>
		</div>
	</section>
	<section class="px-10 pb-11 md:px-32 md:pb-28">
		<div class="flex justify-center">
			<div class="text-white text-6xl hakuna-sans font-bold">
				<span class="block">MEASURE YOUR PROGRESS</span>
			</div>
		</div>
		<div class="flex justify-center">
			<div class="pt-20 flex max-w-[1400px] flex-col-reverse xl:flex-row items-center">
				<div class="mt-12 md:mt-0 md:mr-12 flex justify-center flex-col">
					<span class="block text-white text-2xl nunito">See your progress unfold!</span>
					<span class="block text-[#b5b5b5] text-xl nunito mt-2"
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
			<div class="text-white text-6xl hakuna-sans font-bold">
				<span class="block">JOIN OUR COMMUNITY</span>
			</div>
		</div>
		<div class="flex justify-center">
			<div class="pt-20 flex max-w-[1400px] flex-col xl:flex-row items-center">
				<img loading="lazy" src={img_joinourcommunity} alt="" class="md:max-h-80 w-fit" />
				<div class="mt-12 md:mt-0 md:ml-12 flex justify-center flex-col">
					<span class="block text-white text-2xl nunito">Be a part of something great!</span>
					<span class="block text-[#b5b5b5] text-xl nunito mt-2"
						>Connect with like-minded individuals, share your journey, and get inspired. Together,
						we're building a supportive space for all fitness enthusiasts. Join us and let's achieve
						our goals together!
					</span>
				</div>
			</div>
		</div>
	</section>
</main>
