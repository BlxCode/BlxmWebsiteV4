<script>
  import favicon from "$lib/assets/favicon.png";
  import "../app.css";

  let { children } = $props();
</script>

<svelte:head>
  <title>Blxm</title>
  <link rel="icon" href={favicon} />

  <meta type="description" content="Blxm's Website" />

  <meta name="keywords" content="Blxm, BloxdMaster, BlxCode" />

  <meta name="author" content="Blxm" />
  <meta name="robots" content="index, follow" />
  <link rel="canonical" href="https://www.blxm.me" />

  <meta property="og:title" content="Blxm's Website" />
  <meta
    property="og:description"
    content="Blxm's Website. I am a self proclamed developer, YouTuber, and quite frankly an idiot."
  />
  <meta property="og:image" content={favicon} />
  <meta property="og:url" content="https://blxm.me/" />
  <meta property="og:type" content="website" />

 <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:title" content="Blxm's Website" />
  <meta
    name="twitter:description"
    content="Blxm's Website. I am a self proclamed developer, YouTuber, and quite frankly an idiot."
  />
  <meta name="twitter:image" content={favicon} />


  <script
    src="https://kit.fontawesome.com/d2a23fcf0d.js"
    crossorigin="anonymous"
  ></script>
</svelte:head>

{@render children()}
