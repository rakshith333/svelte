
<script>

  import BackToTop from "./BackToTop.svelte";
  export let autoplay;
  let scY;


</script>

<div class="relative mx-auto pt-12 md:pt-16 xl:pt-0 justify-center hero">
    <div class="videowrapper flex flex-wrap lg:flex" style="-webkit-mask-image: -webkit-gradient(linear, left 80%, left bottom, from(rgba(0,0,0,1)), to(rgba(0,0,0,0)))">
      <video
        id="myvideo1"
        loop
        autoplay="true"
        crossorigin=true
        muted
        playsinline
        class="mx-auto object-cover"
        style="controls:hidden; width:100vw;"
      >
      <track kind="captions"> 
        <!-- <source src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.mp4" type="video/mp4" /> -->
        <!-- <source src="https://spaces.renderpub.com/Boat_13.mp4" type="video/mp4" /> -->
        <source src="../../HeroVideo/HERO.mp4" type="video/mp4">
      </video>
    </div>
    <!-- <video
    class="mx-auto object-cover"
    style="controls:hidden; width:100vw;">		
		<track kind="captions" />
		<source src="HERO.webm" type="video/webm">
		<source src="HERO.mp4" type="video/mp4"> 

	</video>	 -->
    <div class="w-full flex justify-center">
      <div class="absolute text-gray-200 2xl:bottom-44 lg:bottom-24 md:bottom-8 lg:block hidden inset-x-1/2">
        {#if scY<=100}
          <div  id="scroll-down-animation">
              <span class="mouse h-12 w-6">
                <span class="move"></span>
              </span>
            </div>
        {/if}
      </div>
    </div>

    <div class="w-full flex justify-center">
      <!-- <div class="absolute text-gray-200 sm:bottom-1/4 bottom-4 block left-5/11 -ml-10 sm:-ml-8 lg:-ml-4 xl:-ml-1 2xl:ml-4 2xl:mb-6"> -->
      <div class="absolute text-gray-200 sm:bottom-1/4 bottom-4 block 2xl:mb-6 mx-auto"> 
        <button id="TrailerButton" class="border-3 rounded-full watchbtn p-2 font-bold">
          <a href="https://youtu.be/dRr5fF3VIh4" class="a-color" target="_blank">
          Watch Trailer
          </a>
        </button>
      </div>
    </div>
    <!-- <div
      class="absolute xl:text-7xl md:text-5xl sm:text-3xl text-xl xl:p-32 md:p-8 px-2"
      style="margin-top:-50%; text-shadow: 1px 0 50px rgba(0,0,0,1); color:#ffffff;"
    >
      The Complete <br> Architectural <br>Visualization <br>Toolkit <br>

      <button
        id="ClickSubscribeButton"
        class="focus:outline-none bg-our-blue sm:py-3 lg:px-8 sm:px-2 p-1 font-bold rounded text-white hover:ring-2 hover:ring-our-blue lg:text-lg sm:text-base text-sm sm:mt-8 mt-2 sm:ml-2 bg-opacity-100"
        style="color:white;"
      >
        <a href="#signupsection">Subscribe</a>
      </button>
    </div> -->
  </div>
  <svelte:window bind:scrollY={scY} />


<style scoped>
/* VVV Everything you need VVV */

#scroll-down-animation {
  position: absolute;
  margin-top:-0.9em;
  /* top: 20%; */
  left: 50%;
  transform: translate(-50%,-50%);
}
.hero{
  width:100%;
}
/*h2{
  color: #fff;
  font-family: 'Roboto', 'Arial', sans-serif;
  font-weight: 200;
  font-size: 16px;
}*/

.mouse {
  margin: 0 auto;
  display: block;
  border-radius: 50px;
  border: 3px solid #fff;
  /* height: 100px;
  width: 50px; */
  position: relative;
}

.move {
  position: absolute;
  background-color: #fff;
  height: 10px;
  width: 10px;
  border-radius: 50%;
  left: 50%;
  transform: translateX(-50%);
  animation: move 2s linear infinite;
}
.watchbtn{
  border: 3px solid white;
}
.a-color{
  color: white;
  text-decoration: none;
}

@keyframes move {
  0% {
    transform: translate(-50%,5px);
    opacity: 0;
  }
  50% {
    transform: translate(-50%,20px);
    opacity: 1;
  }
  100% {
    transform: translate(-50%,30px);
    opacity: 0;
  }
}
</style>
