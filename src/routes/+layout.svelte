<script>
	import '../app.css';
	import {Nav, Footer} from '../lib';

</script>

<main class="relative">
  <Nav />
	<slot />
	<section class="bg-black padding-x padding-t pb-8">
		<Footer />
	</section>
</main>
