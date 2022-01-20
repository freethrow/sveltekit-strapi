<script>
  import "../app.css";
  import Navbar from "../components/Navbar.svelte";
  import Footer from "../components/Footer.svelte";
</script>

<div class="container mx-auto lg:max-w-screen-md flex flex-col min-h-screen text-gray-600 font-thin">
    <Navbar />
    <div class="flex-1">
        <slot />
    </div>
   
    <Footer />
</div>