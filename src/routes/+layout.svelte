<script>
  import "../app.css";
  import Footer from "../components/Footer.svelte";
  import Header from "../components/Header.svelte";
  import Cta from "../components/Cta.svelte";

  import { openModal } from "../store";

  let y;
  $: outerHeight = 0;

  function reroute(href) {
    $openModal = !$openModal;
    window.location.href = href;
  }
</script>

{#if $openModal}
  <div
    class="fixed top-0 left-0 w-screen h-screen border-b bg-white z-50 flex flex-col gap-8 p-5 px-8"
  >
    <div class="flex items-center justify-between gap-4 border-b pb-2">
      <h1 class="font-semibold">
        Gimmie <span class="text-indigo-400">Gym</span>
      </h1>
      <button
        on:click={() => ($openModal = false)}
        class="outline-none border-none"
      >
        <i class="fa-solid fa-xmark text-2xl"></i>
      </button>
    </div>
    <div class="flex flex-col gap-4 flex-1">
      <button
        on:click={() => reroute("#product")}
        class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
      >
        <p class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold">
          Product <i class="fa-solid fa-chevron-right text-xl pl-4"></i>
        </p>
      </button>
      <button
        on:click={() => reroute("#review")}
        class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
      >
        <p class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold">
          Review <i class="fa-solid fa-chevron-right text-xl pl-4"></i>
        </p>
      </button>
      <button
        on:click={() => reroute("#faq")}
        class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
      >
        <p class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold">
          FAQ <i class="fa-solid fa-chevron-right text-xl pl-4"></i>
        </p>
      </button>
    </div>
    <div class="flex flex-col items-center justify-center"><Cta /></div>
  </div>
{/if}

{#if y > outerHeight}
  <div class="bg-white fixed top-0 left-0 w-full flex flex-col z-20 px-3 fadeIn">
    <Header />
  </div>
{/if}

<slot />
<Footer />
<svelte:window bind:scrollY={y} bind:outerHeight />
