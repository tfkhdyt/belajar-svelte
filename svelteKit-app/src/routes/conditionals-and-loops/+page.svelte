<script lang="ts">
	let products = [
		{ name: 't-shirt', quantity: 10 },
		{ name: 'mug', quantity: 30 },
		{ name: 'sticker', quantity: 8 },
		{ name: 'sweatshirt', quantity: 12 }
	];

	function addProduct() {
		let cup = { name: 'cup', quantity: 4 };
		products = [cup, ...products];
	}
</script>

<button on:click={addProduct}> Add Product </button>
{#each products as product, i (product.name)}
	<h3>{product.name}</h3>
	<input type="checkbox" />
	<div class="bg-blue-500 p-4">{i}</div>
{/each}


<!-- <script lang="ts">
	let product = {
		name: 't-shirt',
		quantity: 0
	};

	function increment() {
		product.quantity++;
	}
</script>

{#if product.quantity > 10}
	<div style="background: lightgreen; padding: 4px;">This product is in stock</div>
{:else if product.quantity === 0}
	<div style="background: lightcoral; padding: 4px;">This item is out of stock</div>
{:else}
	<div style="background: lemonchiffon; padding: 4px;">Only a few items left</div>
{/if}
<h3>Current: {product.name} Quantity: {product.quantity}</h3>
<button on:click={increment}>Increment</button> -->
