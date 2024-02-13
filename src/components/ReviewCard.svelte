<script>
  export let reviewList;
  export let left;
  export let i;
</script>

<div
  class={"flex flex-col gap-2 w-full max-w-[500px] mx-auto relative " +
    (left
      ? i % 2 === 1
        ? " hidden md:flex opacity-0 pointer-events-none max-h-[40px] overflow-hidden"
        : " "
      : i % 2 === 0
        ? " hidden md:flex opacity-0 pointer-events-none max-h-[40px] overflow-hidden"
        : " ")}
>
  <div class="flex relative">
    <div
      class={"absolute rounded-full bg-white aspect-square hidden md:grid place-items-center h-4 top-0 " +
        (i % 2 ===
      0
        ? " right-0 -mr-8 translate-x-1/2"
        : " left-0 -ml-8 -translate-x-1/2")}
    >
      <div class="rounded-full bg-slate-950 aspect-square h-2"></div>
    </div>
    <div class="flex items-center gap-2">
      <i class="fa-solid fa-user"></i>
      <h3 class="text-lg sm:text-xl md:text-2xl">{reviewList.name}</h3>
    </div>
  </div>
  <div class="h-[1.5px] bg-slate-950 w-1/4 mr-auto mb-4 mt-2"></div>
  <div class="flex items-center flex-wrap gap-2 text-xs sm:text-sm mb-4">
    {#each reviewList.features as feature}
      <div
        class="p-1 py-0.5 rounded-md border border-solid border-indigo-400 bg-indigo-50 text-indigo-400"
      >
        <p>{feature}</p>
      </div>
    {/each}
  </div>
  <p>{reviewList.review}</p>
</div>
