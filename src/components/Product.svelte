<script>
  import ProductCard from "./ProductCard.svelte";
  import SectionWrap from "./SectionWrap.svelte";
  let productFeatures = [
    {
      featureList: [
        "Daily Workout",
        "Be Strong",
        "Be Healthy",
        "Effective Work",
      ],
      description:
        "Our premier gym website offers a comprehensive fitness solution, providing daily workout plans to help you build strength, enhance health, and maximize workout effectiveness. Dive into a world of personalized fitness with features like 'Daily Workout,' 'Be Strong,' 'Be Healthy,' and 'Effective Work'.",
      imgUrl: "https://raw.githubusercontent.com/jamezmca/gym-app-landingpage/main/static/assets/selection.png",
    },
    {
      featureList: [
        "Customizable Workouts",
        "Personalized Training",
        "Interactive Challenges",
      ],
      description:
        "Explore a dynamic gym experience through our website, featuring an array of customizable features tailored to your fitness journey. With 'Customizable Workouts,' 'Personalized Training,' and 'Interactive Challenges,' our platform empowers you to tailor your workout routines, track your progress, and engage with a supportive community.",
      imgUrl: "https://raw.githubusercontent.com/jamezmca/gym-app-landingpage/main/static/assets/training.png",
    },
    {
      featureList: [
        "Advanced Tracking",
        "Community Engagement",
        "Exclusive Content Access",
      ],
      description:
        "Embark on a journey of innovation and variety in fitness with our gym website. Discover a diverse range of features designed to elevate your workout routine, including advanced tracking, community engagement, and exclusive content access. With 'Advanced Tracking,' 'Community Engagement,' and 'Exclusive Content Access,' our platform ensures a holistic and engaging fitness experience.",
      imgUrl: "https://raw.githubusercontent.com/jamezmca/gym-app-landingpage/main/static/assets/goal.png",
    },
  ];
</script>

<SectionWrap id="product">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:-bottom-1/4"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        Start Now Be <span class="text-indigo-400">Gimmie</span> With Us
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Features For Anyone
      </h3>
    </div>

    {#each productFeatures as productFeature, i}
      <ProductCard {productFeature} {i}>
        {#if i === 0}
          Experience Exercise <span class="text-indigo-400">Master</span>
        {:else if i === 1}
          Lay All Your Work <span class="text-indigo-400">Routine</span> and Consistent
        {:else}
          Work on Spesific <span class="text-indigo-400">Best</span> Enviroment
        {/if}</ProductCard
      >
    {/each}
  </div>
</SectionWrap>
