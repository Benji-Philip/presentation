<script>
  import SlideOne from "../slides/slideOne.svelte";
  import SlideTwo from "../slides/slideTwo.svelte";
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
</script>

<svelte:window on:keydown={onKeyDown} />
{#if slideNumber === 1}
  <SlideOne />
{/if}
{#if slideNumber === 2}
  <SlideTwo />
{/if}
