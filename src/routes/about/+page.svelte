
<h1>about</h1>
<p>this is the about page.</p>

<script>
	export let images = [
		{
			src: 'https://i0.wp.com/lavidaesunvideojuego.com/wp-content/uploads/2016/09/original4.jpg?fit=1280%2C720&ssl=1',
			alt: 'Imagen de ejemplo',
			caption: 'Ejemplo 1',
			width: 300,
			height: 200,
			href: 'https://i0.wp.com/lavidaesunvideojuego.com/wp-content/uploads/2016/09/original4.jpg?fit=1280%2C720&ssl=1'
		},
		{
			src: 'data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI3NTAiIGhlaWdodD0iMzc1IiB2aWV3Qm94PSIwIDAgNzUwIDM3NSI+PHJlY3Qgd2lkdGg9IjEwMCUiIGhlaWdodD0iMTAwJSIgZmlsbD0iIzJjMzMzNyIvPjwvc3ZnPg==',
			alt: 'Imagen sin enlace',
			caption: 'Ejemplo 2',
			width: 300,
	height: 200
		}
	];
</script>

<style>
	figure {
		margin: 1rem;
		text-align: center;
	}
	img {
		max-width: 100%;
		height: auto;
	}
	figcaption {
		font-size: 0.9rem;
		color: #555;
	}
</style>

{#snippet figure(image)}
	<figure>
		<img src={image.src} alt={image.caption} width={image.width} height={image.height} />
		<figcaption>{image.caption}</figcaption>
	</figure>
{/snippet}

{#each images as image}
	{#if image.href}
		<a href={image.href}>
			{@render figure(image)}
		</a>
	{:else}
		{@render figure(image)}
	{/if}
{/each}

