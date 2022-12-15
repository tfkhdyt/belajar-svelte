<script lang="ts">
	import GridTile from '$lib/GridTile.svelte';
	import type { Product } from '../types/product';

	let products: Product[] = [
		{
			title: 'Mug',
			price: '$10',
			src: 'https://cdn.shopify.com/s/files/1/0434/0285/4564/products/Cup-front-black.png?v=1623159405'
		},
		{
			title: 'Shirt',
			price: '$10',
			src: 'https://cdn.shopify.com/s/files/1/0434/0285/4564/products/short-sleeve-t-shirt-0.png?v=1622902418'
		}
	];

	function updateCost() {
		products[0].price = '$50';
	}
</script>

<main>
	<button on:click={updateCost} class="my-4 bg-pink-500 p-2 text-white">Change Price</button>
	{#each products as product (product.title)}
		<GridTile {product} />
	{/each}
</main>
