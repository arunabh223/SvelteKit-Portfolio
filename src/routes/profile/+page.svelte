<script>
    import experience from '$lib/Experience';
</script>

<svelte:head>
	<title>Arunabh Bora — About</title>
</svelte:head>

<div class="container">
	<main>
		<h1>Profile</h1>
		<p>
			5+ years of experience in tech and operation within the manufacturing and pharma sector.
		</p>
		<h2>Experience</h2>
		{#each Object.entries(experience) as [section, technologies]}
			<ul>
				<li>
					<h4>
						{section}
					</h4>
					<div>
						{#each technologies as technology}
							<div class="list">
								{technology}
							</div>
						{/each}
					</div>
				</li>
			</ul>
		{/each}
	</main>
</div>

<style>
	.container {
		max-width: 900px;
		padding: 0;
		display: flex;
		justify-content: center;
	}

	main {
		max-width: 100%;
		min-height: 500px;
		text-align: left;
		margin: 0 auto;
		box-sizing: border-box;
	}

	h1 {
		font-weight: 700;
		margin: 0 0 50px 0;
		font-size: 36px;
		text-align: start;
	}

	h2 {
		margin-top: 50px;
	}

	.list {
		display: flex;
		flex-direction: column;
		gap: 30px;
        font-size: small;
        font-style: oblique;
	}

	@media (min-width: 900px) {
		.list {
			flex-direction: row;
		}
		main > h1 {
			font-size: 48px;
		}
	}
</style>
