<script>
  import { openModal } from "../store";
</script>

<header class="flex flex-col relative z-20">
  <div
    class="max-w-[1400px] mx-auto w-full flex items-center justify-between p-4 py-6"
  >
    <a href="/">
      <h1 class="font-semibold">
        Gimmie <span class="text-indigo-400">Gym</span>
      </h1>
    </a>
    <button
      on:click={() => ($openModal = true)}
      class="md:hidden grid place-items-center"
    >
      <i class="fa-solid fa-bars"></i>
    </button>
    <nav class="hidden md:flex items-center gap-4 lg:gap-6">
      <a
        href="#product"
        class="duration-200 hover:text-indigo-400 cursor-pointer">Product</a
      >
      <a
        href="#review"
        class="duration-200 hover:text-indigo-400 cursor-pointer">Review</a
      >
      <a href="#faq" class="duration-200 hover:text-indigo-400 cursor-pointer"
        >FAQ</a
      >
      <button class="specialButton">Start Today Buds</button>
    </nav>
  </div>
</header>
