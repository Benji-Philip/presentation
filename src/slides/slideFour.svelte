<script>
    import Image from "../assets/images/valsalva.webp";
    import { onMount } from "svelte";
    import gsap from "gsap";
    onMount(async () => {
      gsap.from(".title-anim", { duration: 1, y: -500, opacity: 0 });
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
      class=" image w-[700px] h-[900px] object-center object-cover rounded-3xl shadow-2xl"
    />
  </div>

  <div class="flex flex-col top-[50px] left-[60px] absolute items-start justify-start mt-[100px]">
  <div
    class=" inline-block text-9xl text-transparent bg-gradient-to-r from-[#ff0f7b] to-[#f89b29] bg-clip-text font-extrabold text-center title-anim"
  >
    Vasalva Test
  </div>
  
  <div
    class="flex flex-col justify-start flex-1 h-full items-start mt-[50px] ml-[30px] gap-[40px]"
  >
    <div
      class=" flex text-4xl font-normal textcontent mt-[10px] text-wrap w-4/6 text-left gap-[6px]"
    >
      <div>&bull;</div>
      <div>
        Build positive pressure in nasopharynx so that air enters the eustachian tube
      </div>
    </div>

    <div
      class=" flex text-4xl font-normal textcontent mt-[10px] text-wrap w-4/6 text-left gap-[6px]"
    >
      <div>&bull;</div>
      <div>
        If air enters the middle ear, the tympanic membrane will move outward
      </div>
    </div>
  
    <div class=" text-4xl font-semibold textcontent">&bull; Avoid in :</div>
    <div class=" text-4xl font-normal textcontent mt-[5px] ml-[60px]">
      &bull; Ventilation
    </div>
    <div class=" text-4xl font-normal textcontent ml-[60px]">
      &bull; Atrophic scar of tympanic membrane
    </div>
    <div class=" text-4xl font-normal textcontent ml-[60px]">
      &bull; Infection in nose and nasopharynx
    </div>
  </div>
</div>