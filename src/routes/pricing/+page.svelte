<script lang="ts">
	import Icon from '@iconify/svelte';
	import { RadioGroup, RadioItem } from '@skeletonlabs/skeleton';

	let annually = false;

</script>
<main class="m-8 mb-32">
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
      class="w-fit h-full grid grid-cols-1 lg:grid-cols-2 justify-center items-center gap-4">
      <div class="card p-6 h-full variant-ghost-surface" >
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
                     <div class="text-sm text-surface-400 {annually ? 'visible' : 'invisible'}">$0 yearly</div>
                  </div>
               </div>
               <div class=" divider-vertical h-20"></div>
               <div>
                  <ul class="space-y-2">
                     <li class="flex items-center space-x-3">
                        <Icon icon="mdi:tick-circle" class="min-w-4"/>
                        <span>Basic Exercise Tracking</span>
                     </li>
                     <li class="flex items-center space-x-3">
                        <Icon icon="mdi:tick-circle" class="min-w-4" />
                        <span>Progress Overview</span>
                     </li>
                     <li class="flex items-center space-x-3">
                        <Icon icon="mdi:tick-circle" class="min-w-4" />
                        <span>General Statistics</span>
                     </li>
                  </ul>
               </div>
            </div>
         </header>
         <footer class="mt-4">
            <div class="w-full text-center">
               <a href="/register" class="btn variant-filled-tertiary w-2/3">Choose plan</a>
            </div>
         </footer>
      </div>
      <div class="relative">
         {#if annually}
         <span class="badge variant-filled-warning absolute top-0 right-0 mt-[-1rem] mr-[-2rem] z-10 text-lg px-4 py-1"
            >-21% OFF 
         </span>
         {/if}
         <div class="card h-full p-6 variant-ghost-surface" >
            <header class="card-header">
               <div class="flex space-x-12 items-center justify-center">
                  <div class="flex flex-col space-y-3 w-[10ch]">
                     <div
                        class="text-sm border border-surface-300 rounded text-surface-300 w-fit px-3 py-1 font-medium"
                        >
                        PREMIUM
                     </div>
                     
                     <div class="h1 font-bold">{#if !annually}$19{:else}$15{/if}</div>
                     <div>
                        Per month
                        <div class="text-sm text-surface-400 {annually ? 'visible' : 'invisible'}">$180 yearly</div>
                     </div>
                  
                  </div>
                  <div class=" divider-vertical h-20"></div>
                  <div>
                     <ul class="space-y-2">
                        <li class="flex items-center space-x-3">
                           <Icon icon="mdi:tick-circle" class="min-w-4" />
                           <span>Personalized Workout Plans</span>
                        </li>
                        <li class="flex items-center space-x-3">
                           <Icon icon="mdi:tick-circle" class="min-w-4"/>
                           <span>Advanced Statistics and Analysis</span>
                        </li>
                        <li class="flex items-center space-x-3">
                           <Icon icon="mdi:tick-circle" class="min-w-4" />
                           <span>Exclusive Training Content</span>
                        </li>
                     </ul>
                  </div>
               </div>
            </header>
            <footer class="mt-4">
               <div class="w-full text-center">
                  <a href="/register" class="btn variant-filled-tertiary w-2/3">Choose plan</a>
               </div>
            </footer>
         </div>
      </div>
   </div>
</main>