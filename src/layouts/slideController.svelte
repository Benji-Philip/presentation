<script>
  import SlideOne from "../slides/slideOne.svelte";
  import SlideTwo from "../slides/slideTwo.svelte";
  import SlideThree from "../slides/slideThree.svelte";
  import SlideFour from "../slides/slideFour.svelte";
  import SlideFive from "../slides/slideFive.svelte";
  import SlideSix from "../slides/slideSix.svelte";
  import SlideSeven from "../slides/slideSeven.svelte";
  import SlideEight from "../slides/slideEight.svelte";
  import SlideNine from "../slides/slideNine.svelte";
  import SlideTen from "../slides/slideTen.svelte";
  import SlideEleven from "../slides/slideEleven.svelte";
  import SlideTwelve from "../slides/slideTwelve.svelte";
  let slideNumber = 1;
  function onKeyDown(e) {
    switch (e.keyCode) {
      case 38:
        //up arrow
        slideNumber += 1;
        console.log(slideNumber);
        break;
      case 40:
        //down arrow
        slideNumber -= 1;
        console.log(slideNumber);
        break;
      case 37:
        //left arrow
        slideNumber -= 1;
        console.log(slideNumber);
        break;
      case 39:
        //right arrow
        slideNumber += 1;
        console.log(slideNumber);
        break;
    }
  }
  function increment() {
    slideNumber += 1;
  }
  function decrement() {
    slideNumber -= 1;
  }
</script>

<svelte:window on:keydown={onKeyDown} />

<div
  class="absolute bottom-0 min-h-full bg-transparent w-full flex flex-0 z-50"
>
  <button on:click={decrement} class="flex flex-[1] bg-transparent"></button>
  <button on:click={increment} class="flex flex-[1] bg-transparent"></button>
</div>
{#if slideNumber === 1}
  <SlideOne />
{/if}
{#if slideNumber === 2}
  <SlideTwo />
{/if}
{#if slideNumber === 3}
  <SlideThree />
{/if}
{#if slideNumber === 4}
  <SlideFour />
{/if}
{#if slideNumber === 5}
  <SlideFive />
{/if}
{#if slideNumber === 6}
  <SlideSix />
{/if}
{#if slideNumber === 7}
  <SlideSeven />
{/if}
{#if slideNumber === 8}
  <SlideEight />
{/if}
{#if slideNumber === 9}
  <SlideNine />
{/if}
{#if slideNumber === 10}
  <SlideTen />
{/if}
{#if slideNumber === 11}
  <SlideEleven />
{/if}
{#if slideNumber === 12}
  <SlideTwelve />
{/if}
