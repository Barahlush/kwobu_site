<script>
  import { onMount } from "svelte";
  import Hero from "$lib/components/Hero.svelte";
  import Navbar from "$lib/components/Navbar.svelte";
  import SectionHeader from "$lib/components/SectionHeader.svelte";
  import Feature from "$lib/components/Feature.svelte";
  import Separator from "$lib/components/Separator.svelte";
  onMount(() => {
    const script = document.createElement("script");
    script.type = "application/ld+json";
    script.textContent = JSON.stringify({
      "@context": "https://schema.org",
      "@type": "SoftwareApplication",
      name: "CanvasPy IDE",
      applicationCategory: "DeveloperApplication",
      operatingSystem: "Web",
      offers: {
        "@type": "Offer",
        price: "0",
        priceCurrency: "USD",
      },
      description:
        "A canvas-based IDE for bootstrapping Python projects and building visual processing pipelines.",
    });
    document.head.appendChild(script);
  });
</script>

<svelte:head>
  <title>Kwobu: Visual Project Builder</title>
  <meta
    name="description"
    content="Bootstrap your Python projects and build processing pipelines visually with CanvasPy IDE. Seamlessly integrate canvas-based design with traditional .py files."
  />
  <link rel="canonical" href="https://www.canvaspyide.com" />
  <meta name="robots" content="index, follow" />
  <link rel="icon" href="/favicon.ico" type="image/x-icon" />
  <link rel="apple-touch-icon" href="/apple-touch-icon.png" />
  <meta
    property="og:title"
    content="CanvasPy IDE: Visual Python Project Builder"
  />
  <meta
    property="og:description"
    content="Bootstrap Python projects and build processing pipelines visually. Seamlessly integrate canvas-based design with traditional .py files."
  />
  <meta
    property="og:image"
    content="https://www.canvaspyide.com/og-image.jpg"
  />
  <meta property="og:url" content="https://www.canvaspyide.com" />
  <meta name="twitter:card" content="summary_large_image" />
</svelte:head>

<div class="polka text-slate-900 font-sans">
  <Navbar />
  <main>
    <Hero />
    <Separator />

    <section
      id="features"
      class="px-32 py-16 flex flex-col justify-center items-center"
    >
      <SectionHeader>Features</SectionHeader>
      <Feature descriptionPosition="left">
        <p slot="description">Jupyter-like runnable cells</p>
        <img
          slot="illustration"
          src="runnable_cell.png"
          alt="CanvasPy IDE Screenshot"
          class="w-1/3"
        />
      </Feature>
      <Separator />
      <Feature descriptionPosition="right">
        <p slot="description">Select any command to run the code</p>
        <img
          slot="illustration"
          src="runnable_cell.png"
          alt="CanvasPy IDE Screenshot"
          class="w-1/3"
        />
      </Feature>
      <Separator />
      <Feature descriptionPosition="top">
        <p slot="description">
          Two-way sync with code files
        </p>
        <img
          slot="illustration"
          src="runnable_cell.png"
          alt="CanvasPy IDE Screenshot"
          class=""
        />
      </Feature>

    </section>

    <section
      id="how-it-works"
      class="px-32 py-16 flex flex-col justify-center items-start"
    >
      <SectionHeader>How it is different from XYZ</SectionHeader>
      <h2 class="scroll-m-20 text-2xl font-medium tracking-tight transition-colors first:mt-0">
        Jupyter Notebook
      </h2>
      <h2 class="scroll-m-20 text-2xl font-medium tracking-tight transition-colors first:mt-0">
        Marimo
      </h2>
      <h2 class="scroll-m-20 text-2xl font-medium tracking-tight transition-colors first:mt-0">
        Dagster
      </h2>
      <h2 class="scroll-m-20 text-2xl font-medium tracking-tight transition-colors first:mt-0">
        VSCode
      </h2>
      <h2 class="scroll-m-20 text-2xl font-medium tracking-tight transition-colors first:mt-0">
        Composio
      </h2>
      <h2 class="scroll-m-20 text-2xl font-medium tracking-tight transition-colors first:mt-0">
        n8n
      </h2>
    </section>

    <section
      id="Download"
      class="px-32 py-16 flex flex-col justify-center items-center"
    >
      <SectionHeader>Downloads</SectionHeader>
      <div class="flex flex-row justify-center items-center gap-16">
        <a href="https://github.com/Barahlush/workflow_builder" class="">
          Download for Windows
        </a>
        <a href="https://github.com/Barahlush/workflow_builder" class="">
          Download for Mac
        </a>
      </div>
    </section>
  </main>

  <footer
    class="px-32 py-16 flex flex-col justify-center items-center text-center"
  >
    <div>
      <p>&copy; 2024 CanvasPy IDE. All rights reserved.</p>
      <ul>
        <li><a href="/privacy">Privacy Policy</a></li>
        <li><a href="/terms">Terms of Service</a></li>
        <li><a href="/contact">Contact Us</a></li>
      </ul>
    </div>
  </footer>
</div>

<style>
  .polka {
    background-image: radial-gradient(
      hsl(214, 32%, 91%) 0.8500000000000001px,
      #ffffff 0.8500000000000001px
    );
    background-size: 16px 16px;
  }
</style>
