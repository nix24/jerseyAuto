<script lang="ts">
  import { fly } from "svelte/transition";
  import "../app.pcss";

  import type { PageData } from "./$types";
  let currentYear = new Date().getFullYear();

  export let data: PageData;
</script>

<body class="flex flex-col h-screen">
  <nav class="navbar bg-base-100 sticky top-0 z-10">
    <div class="navbar-start">
      <a href="/#hero" class="btn btn-ghost text-xl">Logo</a>
    </div>
    <div class="navbar-center hidden lg:flex">
      <ul class="menu menu-horizontal px-1">
        <li><a href="/#about">About</a></li>
        <li><a href="/#services">Services</a></li>
        <li><a href="/#reviews">Reviews</a></li>
        <li><a href="/#gallery">Gallery</a></li>
        <li><a href="/contact">Contact</a></li>
      </ul>
    </div>
    <div class="navbar-end">
      <div class="dropdown dropdown-end">
        <div tabindex="0" role="button" class="btn btn-ghost lg:hidden">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-5 w-5"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            ><path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h8m-8 6h16"
            /></svg
          >
        </div>
        <ul
          class="menu menu-sm dropdown-content mt-3 z-[1] p-2 shadow bg-base-100 rounded-box w-52"
        >
          <li><a href="/#about">About</a></li>
          <li><a href="/#services">Services</a></li>
          <li><a href="/#reviews">Reviews</a></li>
          <li><a href="/#gallery">Gallery</a></li>
          <li><a href="/contact">Contact</a></li>
        </ul>
      </div>
    </div>
  </nav>

  {#key data.url}
    <main
      in:fly={{ y: -200, duration: 300, delay: 300 }}
      out:fly={{ y: 200, duration: 300 }}
      class="flex-1 overflow-y-auto"
    >
      <slot />
    </main>
  {/key}

  <footer
    class="footer footer-center bg-neutral text-neutral-content mx-auto py-4"
  >
    <aside>
      &copy; {currentYear} JerseyAutoRepairs. All rights reserved.
    </aside>
  </footer>
</body>

<style>
  body {
    scroll-behavior: smooth;
    /* set global font to oswald */
    font-family: "Oswald", sans-serif;
  }
</style>
