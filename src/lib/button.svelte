<script>
  export let label;
	export let iconURL;
  export let backgroundColor
  export let textColor
  export let borderColor
  export let fullWidth
</script>

<button class={`
    flex justify-center items-center gap-2 px-7 py-4 border font-montserrat text-lg leading-none
    ${
        backgroundColor
          ? `${backgroundColor} ${textColor} ${borderColor}`
          : "bg-coral-red text-white border-coral-red"
      } rounded-full ${fullWidth && "w-full"}`}
    >
  {label}

  {#if iconURL}
    <img src={iconURL} alt="arrow right icon" class="ml-2 rounded-full w-5 h-5">
  {/if}
</button>
