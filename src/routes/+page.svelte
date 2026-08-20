<script>
    import { onMount } from 'svelte';

    import { ScrollTrigger } from 'gsap/ScrollTrigger';
    import gsap from 'gsap';

    onMount(() => {
        gsap.registerPlugin(ScrollTrigger) 
        gsap.fromTo(".title",
        {
            scale: 0,
            opacity: 0
        },
        {
            scale: 1,
            opacity: 1,
            duration: 0.67,
            ease: "power2.out",
            stagger: { amount: 0.6, from: "random" }
        }
        );
    })
</script>

<div class="h-screen bg-red-500 flex items-center justify-center">
    <div class="w-3/4 h-full grid grid-cols-5 grid-rows-8 gap-1 p-4">
        <!-- Main Name -->
        <div class="title col-start-3 row-start-3 col-span-4 row-span-2 bg-[#C9A6F0]"></div>

        <!-- Sydney Map -->
        <div class="title col-start-5 row-start-1 col-span-2 row-span-2 bg-[#8932ec]"></div>

        <!-- Hackclub -->
        <div class="title col-start-3 row-start-2 col-span-2 row-span-1 bg-[#8932ec]"></div>

        <!-- Web Dev -->
        <div class="title col-start-3 row-start-1 col-span-2 row-span-1 bg-[#8932ec]"></div>

        <!-- Skills -->
        <div class="title col-start-1 row-start-1 col-span-2 row-span-4 bg-[#8932ec]"></div>

    </div>
</div>

<style>
  .title {
    opacity: 0;
  }
</style>
