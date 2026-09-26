<script>
  import Navbar from "$lib/navbar.svelte";
  import Header from "$lib/header.svelte";
  import About from "$lib/about.svelte";
  import Contact from "$lib/contact.svelte";
</script>

<Navbar class="sticky" />
<Header />
<About />
<Contact />
<style lang="postcss">
  :global(body) {
    background-color: var(--color-gray-800);
    user-select: none;
    color: var(--color-white);
  scroll-behavior: smooth;
  }
  :global(html) {
    scroll-behavior: smooth;
  }
 

</style>
