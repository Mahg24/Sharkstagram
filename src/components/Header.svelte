<script>
	export let icons;
	let handlelogos = icons.Modyfier;
</script>

<header class="Header">
	<div class="Header-container">
		<div class="Header-content">
			<div class="Header-toggle center">
				<label class="switch">
					<input id="logos" type="checkbox" on:change={handlelogos} />
					<span class="slider round" />
				</label>
			</div>
			<div class="Header-logo">
				<img src="public/assets/img/logo.svg" alt="" />
			</div>
			<div class="Header-Search-bar center">
				<input class="searh-bar" type="text" />
			</div>
			<div class="Header-nav">
				<ul>
					<li><img src="public/assets/icons/{icons.Home}.svg" alt="" /></li>
					<li><img src="public/assets/icons/{icons.Send}.svg" alt="" /></li>
					<li><img src="public/assets/icons/{icons.Like}.svg" alt="" /></li>
				</ul>
			</div>
		</div>
	</div>
</header>

<style>
	.searh-bar {
		height: 35px;
		width: 300px;
		border-radius: 10px;
		border: none;
	}
	.Header-Search-bar {
		display: flex;
	}
	.Header-toggle {
		display: flex;
	}
	/* The slider */
	.slider {
		position: absolute;
		cursor: pointer;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		background-color: #ccc;
		-webkit-transition: 0.4s;
		transition: 0.4s;
	}

	.slider:before {
		position: absolute;
		content: "";
		height: 26px;
		width: 26px;
		left: 4px;
		bottom: 4px;
		background-color: white;
		-webkit-transition: 0.4s;
		transition: 0.4s;
	}

	input:checked + .slider {
		background-color: #2196f3;
	}

	input:focus + .slider {
		box-shadow: 0 0 1px #2196f3;
	}

	input:checked + .slider:before {
		-webkit-transform: translateX(26px);
		-ms-transform: translateX(26px);
		transform: translateX(26px);
	}

	/* Rounded sliders */
	.slider.round {
		border-radius: 34px;
	}

	.slider.round:before {
		border-radius: 50%;
	}
	.switch input {
		opacity: 0;
		width: 0;
		height: 0;
	}

	.switch {
		position: relative;
		display: inline-block;
		width: 60px;
		height: 34px;
	}
	.Header-content {
		display: flex;
		justify-content: space-around;
	}
	.Header {
		padding: 0.7em;
		width: 100%;
		background-color: #aed5d9;
	}
	ul {
		display: flex;
		text-decoration: none;
		list-style: none;
		margin: 0;
		padding: 0;
	}
	ul li img {
		height: 45px;
		width: 45px;
	}
	li {
		margin: 0 0 0 90px;
	}
</style>
