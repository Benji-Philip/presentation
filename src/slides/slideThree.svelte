<script>
    import { onMount } from "svelte";
        import gsap from "gsap";
        onMount(async () => {
          gsap.from(".title-anim", {duration:1, y: 500,opacity:0 });
        });
    </script>
    
    <div class="flex flex-col flex-1 h-full justify-center title-anim">
      <div
        class=" inline-block text-9xl text-transparent bg-gradient-to-r from-[#ff0f7b] to-[#f89b29] bg-clip-text font-extrabold text-center"
      >
        Anatomy
      </div>
    </div>
    