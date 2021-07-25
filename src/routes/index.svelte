<script lang="ts">
  import LinkListItem from "$lib/components/LinkListItem.svelte";
</script>
<template>
	<section class="pt-0.5rem flow-vertical">
		<header class="container from-sm flow-vertical">
			<h1>Hi, this is dodi!</h1>
			<p class="text-block">
				I'm a web developer, focused on frontend development. I use Svelte(Kit) to build my
				projects, and Elixir in case I need to use a backend. I also rant <em>a lot</em>
				on Twitter about many things, and I sometimes post in Turkish for practice. My sites are below!
			</p>
		</header>
		<main class="container flow-vertical from-sm">
			<h2>My sites</h2>
			<ul class="list flow-vertical">
        <LinkListItem link="https://portfolio.dodiameer.tk" brand="{false}">
          Portfolio
        </LinkListItem>
        <LinkListItem link="https://blog.dodiameer.tk" brand="{false}">
          Blog
        </LinkListItem>
				<LinkListItem link="https://twitter.com/RandomDodi" brand="twitter">
          Twitter (@RandomDodi)
        </LinkListItem>
			</ul>
		</main>
	</section>
</template>

<style lang="postcss">
	.list {
		list-style: none;
	}
</style>
