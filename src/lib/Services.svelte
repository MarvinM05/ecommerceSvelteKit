<script>
  import {services} from '../constants'
  import ServiceCard from './serviceCard.svelte';
</script>

<section class='max-container flex justify-center flex-wrap gap-9'>
  {#each services as service}
    <ServiceCard key={service.label} {...service}/>
  {/each}
</section>