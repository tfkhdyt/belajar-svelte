<script>
	let quantity = 0;
	let inventory = [1, 2, 3];
  let user = { name: 'Taufik' };
  $: remaining = 10 - quantity;
  let price = 5;
  $: totalCost = quantity * price;

	const addToCart = () => {
    inventory = [...inventory, quantity];
		quantity++;
    user.name = 'Hidayat';
	};

  const increasePrice = () => {
    price += 2;
  }
</script>

<h1>Your shopping cart has {quantity} items.</h1>
<button on:click={addToCart}> Add to Cart </button>

<h2>{inventory}</h2>
<h2>{user.name}</h2>
<div>Remaining inventory: {remaining}</div>
<div>Item price: {price}</div>
<button on:click={increasePrice}>Increase price</button>
<div>Total cost: {totalCost}</div>
