<script>
  export let label;
	export let iconURL;
</script>

<button class="flex justify-center bg-coral-red rounded-full text-white border-coral-red items-center gap-2 px-7 py-4 font-montserrat text-lg leading-none">
  {label}
  <img src={iconURL} alt="arrow right icon" class="ml-2 rounded-full w-5 h-5">
</button>
