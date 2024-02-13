<script>
  export let i;
  export let productFeature;
</script>

<div
  class="grid grid-cols-1 md:grid-cols-2 gap-14 md:gap-16 lg:gap-20 relative text-base"
>
  <div
    class={"flex flex-col gap-8 md:gap-10 pt-10 " +
      (i % 2 === 1 ? " md:order-2" : " ")}
  >
    <h4
      class="text-2xl sm:text-3xl md:text-4xl max-w-[1000px] w-full font-medium pr-10 relative after:absolute after:top-full after:left-0 after:w-1/5 after:h-1.5 after:mt-1 after:bg-slate-900"
    >
      <slot />
    </h4>
    <p>{productFeature.description}</p>
    <div class="flex flex-col gap-3">
      {#each productFeature.featureList as listItem}
        <div class="flex gap-2 items-center">
          <div
            class="grid place-items-center p-1.5 text-xs sm:text-sm aspect-square rounded-full border-[1.5px] bg-white border-solid border-green-300"
          >
            <i class="fa-solid fa-bolt  text-green-400"></i>
          </div>
          {listItem}
        </div>
      {/each}
    </div>
    <div class="flex items-center">
      <button class="specialButtonDark mr-auto font-semibold ">
        <p>Try Today &rarr;</p>
      </button>
    </div>
  </div>
  <div class={"flex flex-col dropShadow overflow-hidden rounded-b-lg "}>
    <div
      class="rounded-t-xl h-8 sm:h-10 bg-white opacity-60 flex items-center gap-2"
    >
      {#each [1, 2, 3] as i}
        <div
          class="rounded-full aspect-square w-2.5 sm:w-3 bg-indigo-300 ml-2"
        ></div>
      {/each}
    </div>
    <div class="flex flex-col gap-4 flex-1">
      <img src={productFeature.imgUrl} alt="product-img" />
    </div>
  </div>
</div>
