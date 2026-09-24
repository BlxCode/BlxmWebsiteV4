<script>
  import Navbar from "$lib/navbar.svelte";
  import Header from "$lib/header.svelte";
  import Contact from "$lib/contact.svelte";
</script>

<Navbar />
<Header />
<Contact />
<style lang="postcss">
  :global(body) {
    background-color: var(--color-gray-800);
    user-select: none;
    color: var(--color-white);
  }

</style>
