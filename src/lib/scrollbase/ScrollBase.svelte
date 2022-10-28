<script>
  import MediaQuery from '$lib/mediaquery/MediaQuery.svelte';

    export let el= '#app';
    export let scTimer= 0;
    export let scY= 0;
    


  function handleScroll() {
      if (scTimer) return
        scTimer = window.setTimeout(() =>{
        scY = window.scrollY
        clearTimeout(scTimer)
        scTimer = 0
      }, 100)
    }

    function mounted() {
        window.addEventListener('scroll', handleScroll);
    }

    function toTop(){
      window.scrollTo({
        top: 0,
        behavior: 'smooth'
      })
    }

</script>



<div id="container">
    <slot></slot>
    <!-- v-show="scY > 100" -->

    <transition name="fade">
      {#if scY>100}
        <div id="pagetop" class="fixed block bg-transparent z-30 right-4 bottom-12 svg-container rounded-full border-2 border-white" on:click={toTop}>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            fill="none"
            stroke="#ffffff"
            stroke-width="1.5"
            stroke-linecap="square"
            stroke-linejoin="round"
            id="svg-button"
          >
            <path d="M18 15l-6-6-6 6" />
          </svg>
        </div>
      {/if}      
    </transition>
  </div>
  <svelte:window bind:scrollY={scY} />

  <MediaQuery query="(min-width: 640px)" let:matches>
    {#if matches}
        <style>
          .svg-container{
            width:2.5em;
          }
        </style>
    {/if}
  </MediaQuery>

  <MediaQuery query="(max-width: 639px)" let:matches>
    {#if matches}
        <style>
          .svg-container{
            width:1.7em;
          }
        </style>
    {/if}
  </MediaQuery>


  <style scoped>
    #pagetop:hover {
      cursor: pointer;
    }
    
    

  
        
      
    </style>