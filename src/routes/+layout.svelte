<script>
	let { children } = $props();
	
</script>

<nav>
	<a href="/">home</a>
	<a href="/blog">blog</a>
	<a href="/about">about</a>

</nav>

{@render children()}
