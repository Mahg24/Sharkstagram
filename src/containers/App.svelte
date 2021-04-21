<script>
	import Header from "../components/Header.svelte";
	import Main from "../components/Main.svelte";
	import Timeline from "../components/Timeline.svelte";
	import Sidebar from "../components/Sidebar.svelte";
	let homeIcon = "home";
	let sendIcon = "send";
	let heartIcon = "like";
	let commentIcon = "comment";
	let icons = {
		Home: homeIcon,
		Send: sendIcon,
		Like: heartIcon,
		Comment: commentIcon,
		Modyfier: handlelogos,
	};
	function handlelogos() {
		if (document.querySelector("#logos").checked) {
			icons.Home += "-sea-active";
			icons.Send += "-sea-active";
			icons.Like += "-sea-active";
			icons.Comment += "-sea-active";
		} else {
			icons.Home = "home";
			icons.Send = "send";
			icons.Like = "like";
			icons.Comment = "comment";
		}
	}
</script>

<Header {icons} />
<Main>
	<Timeline {icons} />
	<Sidebar />
</Main>

<style>
	:global(html) {
		box-sizing: border-box;
		font-size: 16px;
	}
	:global(body) {
		background-color: #6daebb;
		color: white;
		margin: 0;
		padding: 0;
	}
	:global(.center) {
		justify-content: center;
		align-items: center;
	}
</style>
