<script>
	export let icons;
</script>

<div class="Card">
	<div class="Card-container">
		<div class="Card-header">
			<div class="Card-user">
				<div class="Card-user-img">
					<img class="Profile-pic" src="public/assets/img/profile.jpg" alt="" />
				</div>
				<h2>Shark King</h2>
			</div>
			<div class="Card-settings"><h1>...</h1></div>
		</div>
		<div class="Card-Photo">
			<img src="public/assets/img/shark.jpg" alt="" />
		</div>
		<div class="Card-icons">
			<img src="public/assets/icons/{icons.Home}.svg" alt="" />
			<img src="public/assets/icons/{icons.Send}.svg" alt="" />
			<img src="public/assets/icons/{icons.Like}.svg" alt="" />
		</div>
	</div>
</div>

<style>
	.Card-header {
		display: flex;
		justify-content: space-around;
	}
	.Card {
		width: 50%;
		background-color: white;
		color: #040b23;
		display: flex;
		padding: 10px;
	}
	.Card-user {
		display: flex;
		align-items: center;
	}
	.Card-user span {
		align-self: flex-start;
	}
	.Card-user h2 {
		margin: 20px;
	}
	.Card-user-img {
		margin: 10px;
		width: 70px;
		height: 70px;
		border-radius: 50%;
		overflow: hidden;
		border: solid #073f71 5px;
	}
	.Card-user img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
	.Card-Photo img {
		max-width: 450px;
	}
</style>
