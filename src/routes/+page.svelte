<script>
  import About from "$lib/about.svelte";
  import Navbar from "$lib/navbar.svelte";
  import Header from "$lib/header.svelte";
  import Projects from "$lib/projects.svelte";
  import Contact from "$lib/contact.svelte";
  import TechStack from "$lib/techStack.svelte";
</script>

<Navbar class="sticky" />

<Header />
<About />
<TechStack />
<Projects />
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
