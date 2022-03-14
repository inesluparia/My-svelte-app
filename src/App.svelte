<script>
	import ContentSection from "./Section/ContentSection.svelte"
	import MessageEditor from "./MessageEditor/MessageEditor.svelte"
	
</script>

<main>
	
	<h1 id="message">Hello!</h1>
	
	<MessageEditor/>
	
	<hr>

	<ContentSection/>

</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
	button {
		color: #118bee;
	}

	button:active {
		/* Darken on click by 15% (down to 85%) */
		filter: brightness(0.85);
	}
</style>