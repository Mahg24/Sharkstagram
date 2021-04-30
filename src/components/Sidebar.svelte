<script>
	import Profile from "./Profile.svelte";
	import Stories from "./Stories.svelte";
	import Footer from "./Footer.svelte";
</script>

<div class="Sidebar">
	<div class="Sidebar-container">
		<Profile />
		<Stories />
		<Footer />
	</div>
</div>

<style>
	.Sidebar-container
	{
	position: fixed;
    top: 90px;
    right: 280px;
	}
</style>
