<script>
  export let dark;
</script>

<div class="flex items-center gap-4">
  <button class={"specialButton " + (dark ? " bg-[#181b34]" : " ")}>
    <p class="text-base sm:text-lg md:text-xl">Contact Us</p>
  </button>
  <button class={"specialButtonDark"}>
    <p class="text-base sm:text-lg md:text-xl">Get Started &rarr;</p>
  </button>
</div>
