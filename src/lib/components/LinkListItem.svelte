<script lang='ts'>
  export let brand: string | false;
  export let link: string;
</script>
<template>
  <li class="list-item {brand || "no-brand"}">
    <a
      href="{link}"
      target="_blank"
      rel="noopener noreferrer"
      class="list-item__content flow-horizontal"
    >
    {#if brand}
      <i class="list-item__icon fab fa-{brand}" />
    {/if}
      <p class="list-item__name"><slot /></p>
    </a>
  </li>
</template>

<style lang='postcss'>
  .list-item {
    border: 4px solid var(--shade-dark);
		transition: 0.15s ease-out;
		transition-property: border-color, color;
    box-shadow: 0 0.25rem 0.25rem rgba(0, 0, 0, 0.25);
	}
  
	.list-item__content {
    display: flex;
		align-items: center;
		color: currentColor;
		text-decoration: none;
		font-weight: bold;
    padding: 0.75rem 1.25rem;
    --flow-horizontal: 0.75em;
	}

  .list-item__content > * > * {
    --flow-horizontal: var(--flow-default);
  }

	.list-item__name {
		flex: 1;
	}

	.list-item:hover, .list-item:focus-within, .list-item:focus {
		border-color: var(--brand-color);
		color: var(--brand-color);
	}

  .list-item:focus, .list-item > *:focus {
    /*! This is fine because our border changes !*/
    outline: none;
  }

  /* purgecss start ignore */
	.list-item:global(.twitter) {
    --brand-color: #15aabf;
	}
  .list-item:global(.no-brand) {
    --brand-color: var(--shade-primary-500-color);
	}
  /* purgecss end ignore */
</style>