<script>
	export let imgURL;
	export let changeBigShoeImage;
	export let bigShoeImg;

	const handleClick = () => {
		console.log('click');
		if (bigShoeImg !== imgURL.bigShoe) {
			changeBigShoeImage(imgURL.bigShoe);
		}
	};
</script>

<div
	class={`border-2 rounded-lg
		${bigShoeImg === imgURL.bigShoe ? 'border-color-red' : 'border-transparent'}
		cursor-pointer max-sm:flex-1`}
	on:click={handleClick}
>
	<div
		class="flex justify-center items-center bg-card bg-center bg-cover sm:w-40 sm:h-40 rounded-lg max-sm:p-4 border-2"
	>
		<img
			src={imgURL.thumbnail}
			alt="shoe collection"
			width={127}
			height={103}
			class="object-contain"
		/>
	</div>
</div>
