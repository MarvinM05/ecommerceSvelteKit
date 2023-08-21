<script>
  import {headerLogo} from '../assets/images'
  import {hamburger} from '../assets/icons'
  import {navLinks} from '../constants'
</script>

<header class="padding-x py-8 absolute z-10 w-full">
  <nav class="flex justify-between items-center max-container">
    <a href="/">
    <img src={headerLogo} alt="Logo" width={130}
    height={29}></a>
    <ul class="flex-1 flex justify-center items-center gap-16 max-lg:hidden">
      {#each navLinks as item}
        <li key={item.label}>
        <a href={item.href} class="font-monserrats leading-normal text-lg text-slate-gray">
        {item.label}</a></li>
      {/each}
    </ul>
    <div class="hidden max-lg:block">
      <img src={hamburger} alt="hamburger" width={25} height={25}>
    </div>
  </nav>
</header>