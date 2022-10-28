<script>
    import { page } from '$app/stores';
    import Viewer from '$lib/viewer/Viewer.svelte';
    console.log("this prints")
    console.log($page.params.userID);
    console.log($page.params.projectID);

</script>


<svelte:head>
	<title>Spaces</title>
</svelte:head>



<Viewer userID={$page.params.userID} projectID={$page.params.projectID} startScene=0 startHotspot="Hotspot0" />
