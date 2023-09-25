<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
	
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<button id="nob">Duplicate</button>
	<button id="background-color">Change Background Color</button>
	<button id="change-heading">Change Heading Text</button>
	<button id="delete-last-card">Delete Last Card</button>
	
	<div class="grid">
	  <div class="card">
			<img src="https://images.unsplash.com/photo-1586957960772-3e526c5e7cbd?crop=entropy&cs=srgb&fm=jpg&ixid=M3wzMjM4NDZ8MHwxfHJhbmRvbXx8fHx8fHx8fDE2OTM0OTY0NDF8&ixlib=rb-4.0.3&q=85" style="width:100%">
			<h2>Christian Wasta</h2>
			<p>Destroyer of Worlds. HAX is a paradigm shift for web publishing. It puts advanced authoring capabilities in the hands of everyone, regardless of technical ability and all items made are sustainability built in highly semantic HTML. </p>
			<div class="button">
			<button tabindex="-1" id="details">Details</button>
			</div>                                          
	   </div>
	</div>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}	
	
	.card{
		margin: 0 auto;
		max-width: 300px;
		max-height: 400px;
		min-height: 10px;
		padding: 8px 8px 28px 8px;
		border-radius: 10px;
		overflow: hidden;
		background-color: beige;
	}

	a {
		text-decoration: none;
		text-align: center;
		color: black;
	}

	.grid {
		display: grid;
		grid-template-columns: repeat(1, 1fr);
	}

	#nob:hover, #nob:focus {
		background-color: black;
		color: white;
	}

	@media screen and (max-width: 800px) {
	.button {
		display: none;
		background-color: white;
	}
	}

	@media screen and (max-width: 500px) {
	.card {
		width: 100%;
	}
	}
</style>
