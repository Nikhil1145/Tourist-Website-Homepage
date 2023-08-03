<script>
    import Card from "./Card.svelte";
    import LowerCards from "./LowerCards.svelte";
    import People from "./People.svelte";
    import BottomCards from "./BottomCards.svelte";
    import { fly } from 'svelte/transition';
	  let visible = false;
    let btnVisibility = true;
    function Visibility (){
      visible = true;
      btnVisibility = false;
    }
</script>
<div class="flex flex-col items-center mt-40">
  <h1 class="text-white text-4xl md:text-8xl text-center">
      Switzerland has Never <br> Been So Affordable
  </h1>
</div>

<div class="text-center mt-8">
  <h1 class="text-white text-2xl md:text-3xl">
      Discover Switzerland. Choose the best
  </h1>
  <h1 class="text-white text-2xl md:text-3xl">
      program, guide, hotels and restaurants
  </h1>
</div>

<div class="flex justify-center p-8">
  <button class="flex bg-red-500 hover:bg-red-600 text-white py-2 px-4 rounded w-60 md:w-80 justify-center">
      Start To Explore
  </button>
</div>

<Card />

<div class="mt-8 text-center">
    <h1 class="text-white justify-center flex text-6xl">Top Programs</h1>

    <h1 class="text-slate-300 flex justify-center text-xl pt-8">
        Our programs are compiled by the best Guides. Each tourist <br> will be able to choose a program according to their level
    </h1>
</div>

<div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4 justify-items-center">
  <LowerCards />
  <LowerCards />
  <LowerCards />
  <LowerCards />
  <LowerCards />
  <LowerCards />
</div>



<div class="flex justify-center p-4 md:p-8"> 
  <button class="flex bg-red-500 hover:bg-red-600 text-white py-2 px-4 rounded w-40 md:w-60 justify-center"> 
      Show More
  </button>
</div>




<h1 class="text-white justify-center flex text-3xl md:text-6xl text-center mt-6 md:mt-12"> 
  Emotions are the best you <br> can get in this life
</h1>
<h1 class="text-slate-300 flex justify-center text-base md:text-xl pt-4 md:pt-8 text-center"> 
  Check out the reviews of people who used <br> our services
</h1>


<People />


<h1 class="text-white justify-center flex text-6xl text-center mt-9">Our Guides</h1>
<h1 class="text-slate-300 flex justify-center text-xl pt-8 text-center">
  Our Certified and knowledgeable guides live <br> and breathe the adventure life
</h1>



<div class="grid justify-center align-middle">
  <BottomCards />
{#if visible}
<div class="grid justify-center mt-8" transition:fly={{ y: 20, duration: 700 }}>
  <BottomCards />
</div>


{/if}
{#if btnVisibility}
<div class="flex justify-center mt-8">
  <button on:click={Visibility} class="flex bg-red-500 hover:bg-red-600 text-white py-2 px-4 rounded w-60 md:w-80 justify-center align-middle"  >
    Show More
  </button>
  </div>
{/if}

</div>


<div class="flex justify-center p-8">
  <button class=" flex bg-red-500 hover:bg-red-600 text-white py-2 px-4 rounded w-60 justify-center">
      Get To Know the Team
    </button>
</div>