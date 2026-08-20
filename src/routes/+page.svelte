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

<div class="h-screen bg-ctp-crust flex items-center justify-center">
    <div class="w-3/4 h-full grid grid-cols-5 grid-rows-8 gap-1 p-4">
        <!-- Main Name -->
        <div class="rounded-br-sm border border-dashed border-[#45475a] title col-start-3 row-start-3 col-span-4 row-span-2 bg-ctp-mantle">Main</div>

        <!-- Sydney Map -->
        <div class="rounded-tr-sm border border-dashed border-[#45475a] title col-start-5 row-start-1 col-span-2 row-span-2 bg-ctp-mantle">Sydney</div>

        <!-- Hackclub -->
        <div class="border border-dashed border-[#45475a] title col-start-3 row-start-2 col-span-2 row-span-1 bg-ctp-mantle">HC</div>

        <!-- Web Dev -->
        <div class="border border-dashed border-[#45475a] title col-start-3 row-start-1 col-span-2 row-span-1 bg-ctp-mantle">Web</div>

        <!-- Skills -->
        <div class="rounded-bl-sm rounded-tl-sm border border-dashed border-[#45475a] title col-start-1 row-start-1 col-span-2 row-span-4 bg-ctp-mantle">Skills</div>

    </div>
</div>

<style>
  .title {
    opacity: 0;
  }
</style>
