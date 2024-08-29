<script>
  import ViewPort from "svelte-viewport-info";
  let defaultCanvasW = 1920;
  let defaultCanvasH = 1080;
  let vw = ViewPort.Width;
  let vh = ViewPort.Height;
  let canvasH = 0;
  let canvasW = 0;
  let validW = (defaultCanvasH / 1920) * vw;
  let scale = 1;
  setCanvas();
  function setCanvas() {
    validW = (defaultCanvasH / 1920) * vw;
    vw = ViewPort.Width;
    vh = ViewPort.Height;
    if (vh > validW) {
      canvasW = vw;
      scale = canvasW / defaultCanvasW;
    } else {
      canvasH = vh;
      scale = canvasH / defaultCanvasH;
    }
  }
</script>

<svelte:body on:viewportchanged={setCanvas} />
<div id="scaler" class=" flex flex-0 text-9xl m-0 p-0" style="scale:{scale}">
  <div
    id="canvas"
    class="bg-white flex flex-0 rounded-md m-0 p-0 overflow-clip"
    style="width:{defaultCanvasW}px; height:{defaultCanvasH}px"
  >
    <slot />
  </div>
</div>
