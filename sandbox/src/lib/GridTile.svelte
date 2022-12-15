<script lang="ts">
	import type { Product } from '../types/product';

	export let product: Product = {
		title: 'No product provided',
		src: 'https://img.icons8.com/ios/500/no-image.png',
		price: '$0'
	};
	console.log(product);
</script>

<div class="h-[50vh] w-full overflow-hidden bg-indigo-600">
	<div class="relative flex h-full w-full items-center justify-center">
		<img
			src={product.src}
			class="w-full flex-none transition duration-300 ease-in-out md:w-1/2 lg:w-full"
			alt=""
		/>
		<div class="absolute top-0 left-0 text-white">
			<div class="bg-black p-3 text-2xl font-medium">{product.title}</div>
			<div class="w-fit bg-black p-3 text-sm">{product.price}</div>
		</div>
	</div>
</div>
