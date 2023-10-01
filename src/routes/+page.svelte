<script>
	function changeBackgroundColor() {
		const elem = document.querySelector('.card');
		const backgroundColor = elem.style.backgroundColor;

		if (backgroundColor === 'beige') {
			elem.style.backgroundColor = 'green';
		} else {
			elem.style.backgroundColor = 'beige';
		}
	}

	function duplicateButton() {
		const elem = document.querySelector('.card');
		const clone = elem.cloneNode(true);
		document.body.appendChild(clone);``
	}

	function changeHeading() {
		const elem = document.querySelector('.card h2');
		if (elem.innerHTML === 'Christian Wasta') {
			elem.innerHTML = 'Something Else';
		} else {
			elem.innerHTML = 'Christian Wasta';
		}
	}

	function deleteLastCard() {
		const elem = document.querySelectorAll('.card');
		if (elem.length > 1) {
			elem[elem.length - 1].remove();
		}
	}
</script>

<section>
	<button id="nob" on:click={duplicateButton}>Duplicate</button>
	<button id="background-color" on:click={changeBackgroundColor}>Change Background Color</button>
	<button id="change-heading" on:click={changeHeading}>Change Heading Text</button>
	<button id="delete-last-card" on:click={deleteLastCard}>Delete Last Card</button>

	<div class="grid">
		<div class="card">
			<img
				src="https://images.unsplash.com/photo-1586957960772-3e526c5e7cbd?crop=entropy&cs=srgb&fm=jpg&ixid=M3wzMjM4NDZ8MHwxfHJhbmRvbXx8fHx8fHx8fDE2OTM0OTY0NDF8&ixlib=rb-4.0.3&q=85"
				style="width:100%"
			/>
			<h2>Christian Wasta</h2>
			<p>
				Destroyer of Worlds. HAX is a paradigm shift for web publishing. It puts advanced authoring
				capabilities in the hands of everyone, regardless of technical ability and all items made
				are sustainability built in highly semantic HTML.
			</p>
			<div class="button">
				<button id="details">Details</button>
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

	.card {
		margin: 0 auto;
		max-width: 300px;
		max-height: 400px;
		min-height: 10px;
		padding: 8px 8px 28px 8px;
		border-radius: 10px;
		overflow: hidden;
		background-color: beige;
	}

	.grid {
		display: grid;
		grid-template-columns: repeat(1, 1fr);
	}

	#nob:hover,
	#nob:focus {
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
