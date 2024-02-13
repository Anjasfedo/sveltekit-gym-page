<script>
  import SectionWrap from "./SectionWrap.svelte";
  let faqs = [
    {
      question: "What is Gimmie Gym?",
      ans: "Gimmie Gym is a fun fitness app designed to make your workouts enjoyable by incorporating interactive games and challenges.",
    },
    {
      question: "How do I download Gimmie Gym?",
      ans: "You can download Gimmie Gym from the App Store (for iOS) or Google Play Store (for Android) on your mobile device.",
    },
    {
      question: "Is Gimmie Gym free to use?",
      ans: "Yes, Gimmie Gym offers a free version with basic features. There is also a premium subscription that unlocks additional games and advanced workout tracking.",
    },
    {
      question: "What types of workouts does Gimmie Gym offer?",
      ans: "Gimmie Gym offers a variety of workouts, including cardio, strength training, and flexibility exercises. The workouts are designed to be engaging and entertaining.",
    },
    {
      question: "Can I connect Gimmie Gym to my fitness tracker?",
      ans: "Yes, Gimmie Gym supports integration with popular fitness trackers, allowing you to sync your workout data and track your progress seamlessly.",
    },
    {
      question: "Are there multiplayer features in Gimmie Gym?",
      ans: "Yes, Gimmie Gym includes multiplayer challenges, allowing you to compete with friends or join group workouts for a more interactive and social experience.",
    },
    {
      question: "How does Gimmie Gym motivate users to stay active?",
      ans: "Gimmie Gym employs a reward system, where users earn points and achievements for completing workouts. These rewards can be used to unlock new levels, challenges, and in-app content.",
    },
    {
      question: "Can I customize my workouts in Gimmie Gym?",
      ans: "Absolutely! Gimmie Gym allows users to customize their workouts based on personal preferences, fitness goals, and available equipment.",
    },
    {
      question: "Is there a beginner-friendly mode in Gimmie Gym?",
      ans: "Yes, Gimmie Gym offers a beginner-friendly mode with easier exercises and lower intensity workouts, making it suitable for users at various fitness levels.",
    },
    {
      question: "How often should I use Gimmie Gym for optimal results?",
      ans: "The frequency of Gimmie Gym workouts depends on your fitness goals. It is recommended to engage in at least 3-5 sessions per week for noticeable results.",
    },
  ];
</script>

<SectionWrap id="faq">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        For All Your Questions
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Frequently Asked Questions
      </h3>
    </div>
    <div class="flex flex-col gap-8 sm:gap-10 md:gap-14 w-full">
      {#each faqs as faq}
        <div
          class="flex flex-col gap-2 text-left max-w-[800px] w-full mx-auto relative p-4 px-6"
        >
          <div
            class="absolute top-0 left-0 w-1/3 h-[1px] bg-slate-950 -translate-x-4"
          ></div>
          <div
            class="absolute top-0 left-0 h-2/3 w-[1px] bg-slate-950 -translate-y-4"
          ></div>
          <h4 class="text-lg sm:text-xl md:text-2xl pt-2">{faq.question}</h4>
          <p class="p-2">{faq.ans}</p>
        </div>
      {/each}
    </div>
  </div>
</SectionWrap>
