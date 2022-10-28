<script lang="ts">
	import Counter from '$lib/Counter.svelte';
	import Hero from '$lib/hero/Hero.svelte';
	import CTA1 from '$lib/cta1/CTA1.svelte';
	import CTA2 from '$lib/cta2/CTA2.svelte';
	import SectionHeading from '$lib/sectionheading/SectionHeading.svelte';
	import TimelineUI from '$lib/timelineui/TimelineUI.svelte';
	import Spaces2 from '$lib/spaces2/Spaces2.svelte';
	import SpacesSection from '$lib/spacessection/SpacesSection.svelte';
	import Usecase from '$lib/usecase/Usecase.svelte';
	import Showcase1 from '$lib/showcase1/Showcase1.svelte';
	import Technology from '$lib/technology/Technology.svelte';
	import FAQ from '$lib/FAQ/FAQ.svelte';
	import Footer from '$lib/footer/Footer.svelte';

</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<Hero/>
	<SectionHeading sectionTitle="The Complete Architectural Visualization Toolkit" id="" description="3D Modeling,  Realtime Rendering,  Virtual Reality" Class="lg:pb-32 sm:pb-24 pb-16" />
	<CTA1/>
	<SectionHeading sectionTitle="Workflow" description="" Class="" id="workflow-title" />
	<TimelineUI/> 
	<SectionHeading sectionTitle="Product Suite" description="" id="" Class="pt-16 sm:pt-12 lg:pt-8 sm:-mt-0" />
	<!-- <SpacesSection id="SpacesSection"/> -->
	<Usecase/>
	<SectionHeading id="Showcase" sectionTitle="Showcase" Class="" description="" />
	<Showcase1 />
	<SectionHeading sectionTitle="Technology" Class="" id="" description="Built with the power of Unreal Engine. Made faster with NVIDIA's Deep Learning Super Sampling (DLSS)." />
	<Technology/>
	<CTA2/>
	<SectionHeading id="FAQ" sectionTitle="Frequently Asked Questions" Class="" description="" />
	<FAQ/>
	
	<!-- <h1>
		<span class="welcome">
			<picture>
				<source srcset="svelte-welcome.webp" type="image/webp" />
				<img src="svelte-welcome.png" alt="Welcome" />
			</picture>
		</span>  

		to your latest <br />SvelteKit app1
	</h1>

	<h2>
		try editing <strong>src/routes/index.svelte</strong>
	</h2>

	<Counter /> -->
</section>


<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
	}

	h1 {
		width: 100%;
	}
	*{
		background-color: black;
	}
	#workflow-title{
		
	}
</style>
