<script>
  import ETimage from "../assets/images/ET.webp";
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

<div
  class=" top-[50px] left-[60px] absolute inline-block text-9xl text-transparent bg-gradient-to-r from-[#ff0f7b] to-[#f89b29] bg-clip-text font-extrabold text-center title-anim"
>
  Anatomy
</div>
<div class=" absolute flex flex-col flex-1 h-full justify-center right-[60px]">
  <img
    src={ETimage.src}
    alt=""
    class=" image w-[700px] h-[700px] object-left object-cover rounded-3xl shadow-2xl"
  />
</div>
<div
  class="flex flex-col justify-start flex-1 h-full items-start mt-[220px] ml-[100px] gap-[40px]"
>
  <div class=" text-4xl font-semibold textcontent">&bull; Two Parts:</div>
  <div class=" text-4xl font-normal textcontent mt-[5px] ml-[60px]">
    &bull; <b>bony</b> - posterolateral (12 mm)
  </div>
  <div class=" text-4xl font-normal textcontent ml-[60px]">
    &bull; <b>fibrocartilaginous</b> - anteromedial(24 mm)
  </div>

  <div
    class=" flex text-4xl font-normal textcontent mt-[10px] text-wrap w-1/2 text-left gap-[6px]"
  >
    <div>&bull;</div>
    <div>
      <b>Tympanic end</b> - bony, 5 × 2 mm, anterior wall of middle ear
    </div>
  </div>

  <div
    class=" flex text-4xl font-normal textcontent mt-[10px] text-wrap w-1/2 text-left gap-[6px]"
  >
    <div>&bull;</div>
    <div>
      <b>Pharyngeal end</b> - slit-like, vertical, nasopharynx
    </div>
  </div>

  <div class=" text-4xl font-semibold textcontent">&bull; Functions:</div>
  <div class=" text-4xl font-normal textcontent mt-[5px] ml-[60px]">
    &bull; Ventilation
  </div>
  <div class=" text-4xl font-normal textcontent ml-[60px]">
    &bull; Protection ( against sound pressure &<br>&nbsp;&nbsp; reflux of nasopharyngeal secretions )
  </div>
  <div class=" text-4xl font-normal textcontent ml-[60px]">
    &bull; Clearance
  </div>
</div>
