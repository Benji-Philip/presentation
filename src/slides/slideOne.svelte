<script>
  import { onMount } from "svelte";
  import gsap from "gsap";
  onMount(async () => {
    gsap.from(".title-anim", { duration:1, opacity: 0, y:500, stagger: 0.2});
  });
</script>

<div class="flex flex-col flex-1 h-full justify-center">
  <div class="flex flex-row gap-6 items-center justify-center">
    <div
      class=" inline-block text-9xl text-transparent bg-gradient-to-r from-[#ff0f7b] to-[#f89b29] bg-clip-text font-extrabold text-center title-anim"
    >
      Eustachian
    </div>
    <div
      class=" inline-block text-9xl text-transparent bg-gradient-to-r from-[#ff0f7b] to-[#f89b29] bg-clip-text font-extrabold text-center title-anim"
    >
      Tube
    </div>
  </div><div class="flex flex-row gap-6 items-center justify-center">
    <div
      class=" inline-block text-9xl text-transparent bg-gradient-to-r from-[#ff0f7b] to-[#f89b29] bg-clip-text font-extrabold text-center title-anim"
    >
      Function
    </div>
    <div
      class=" inline-block text-9xl text-transparent bg-gradient-to-r from-[#ff0f7b] to-[#f89b29] bg-clip-text font-extrabold text-center title-anim"
    >
      Tests
    </div>
  </div>
</div>
