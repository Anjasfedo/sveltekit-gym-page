<script>
  import SectionWrap from "./SectionWrap.svelte";
  import Header from "./Header.svelte";
  import Cta from "./Cta.svelte";
  import Star from "./Star.svelte";
</script>

<SectionWrap>
  <Header />
  <div
    class="flex flex-col gap-10 flex-1 items-center justify-center pb-10 md:pb-14"
  >
    <h2
      class="text-5xl sm:text-6xl md:text-7xl lg:text-8xl max-w-[1200px] mx-auto w-full text-center font-semibold"
    >
      <span class="text-indigo-400">Gym</span> Training Is
      <span class="text-slate-600 line-through">Hard</span><br />
      Just Got
      <span class="text-indigo-400">Easier</span>
    </h2>
    <p
      class="text-xl sm:text-2xl md:text-3xl text-center max-w-[1000px] mx-auto w-full"
    >
      Less think & more doing. Do <span class="italic"
        >workouts, exercise, analytic</span
      > and much more.
    </p>
    <Cta />
<Star />
  </div>
</SectionWrap>
