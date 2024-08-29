<script>
    import Image from "../assets/images/mbst.webp";
    import { onMount } from "svelte";
    import gsap from "gsap";
    onMount(async () => {
      gsap.from(".title-anim", { duration: 1, y: 500, opacity: 0 });
      gsap.from(".image", { duration: 1, x: 500, opacity: 0, delay: 0.3 });
      gsap.from(".textcontent", {
        duration: 1,
        y: 500,
        opacity: 0,
        delay: 0.3,
        stagger: 0.3,
      });
    });
  </script>
  
  <div class=" absolute flex flex-col flex-1 h-full justify-center right-[60px]">
    <img
      src={Image.src}
      alt=""
      class=" image w-[800px] h-[400px] object-left object-cover rounded-3xl shadow-2xl"
    />
  </div>

  <div class="flex flex-col top-[50px] left-[60px] absolute items-start justify-start mt-[200px]">
  <div
    class=" text-left inline-block text-8xl text-transparent bg-gradient-to-r from-[#ff0f7b] to-[#f89b29] bg-clip-text font-extrabold title-anim"
  >
  Saccharine or<br>Methylene Blue Test
  </div>
  
  <div
    class="flex flex-col justify-start flex-1 h-full items-start mt-[50px] ml-[30px] gap-[40px]"
  >
    <div
      class=" flex text-4xl font-normal textcontent mt-[10px] text-wrap w-3/5 text-left gap-[6px]"
    >
      <div>&bull;</div>
      <div>
        Saccharine solution or methylene blue placed in the middle ear
      </div>
    </div>

    <div
      class=" flex text-4xl font-normal textcontent mt-[10px] text-wrap w-3/5 text-left gap-[6px]"
    >
      <div>&bull;</div>
      <div>
        Imparts a sweet taste when saccharine solution reaches the nasopharynx
      </div>
    </div>

    <div
      class=" flex text-4xl font-normal textcontent mt-[10px] text-wrap w-3/5 text-left gap-[6px]"
    >
      <div>&bull;</div>
      <div>
        Methylene blue stains the pharyngeal secretions when it reaches the nasopharynx
      </div>
    </div>

  </div>
</div>