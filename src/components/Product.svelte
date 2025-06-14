<script>
    import SectionWrapper from "./SectionWrapper.svelte";
    import ProductCard from "./ProductCard.svelte";
    let productFeatures = [
        {
            featureList: [
                "Daily streak counter",
                "Weights and reps tracker",
                "Community challenges",
                "Every workout is new and exciting",
            ],
            description:
                "Swoley Moley ensures all users have the information they need to train safely and train effectively.",
            imgUrl: "assets/selection.png",
        },
        {
            featureList: [
                "Select your preferences",
                "Personalize your experience",
                "Customize your workouts",
                "Guaranteed to keep you motivated",
            ],
            description:
                "Build your own workout routine with Swoley Moley. Choose from a variety of exercises and customize your training plan to fit your goals.",
            imgUrl: "assets/training.png",
        },
        {
            featureList: [
                "Track your progress",
                "Monitor your performance",
                "Stay accountable",
                "Achieve your fitness goals",
            ],
            description:
                "Swoley Moley helps you stay on track with your fitness journey. Monitor your progress, set goals, and celebrate your achievements.",
            imgUrl: "assets/goal.png",
        },
    ];
</script>

<SectionWrapper id="product">
    <div
        class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14"
    >
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
                Start your lifetime <span class="text-indigo-400"
                    >gym streak</span
                > today
            </p>
            <h3
                class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
            >
                Features for Everyone
            </h3>
        </div>
        {#each productFeatures as productFeature, index}
            <ProductCard {productFeature} {index}>
                {#if index === 0}
                    Experience a beginner exercise <span
                        class="text-indigo-400 font-medium">master</span
                    > class
                {:else if index === 1}
                    Lay the foundations for <span
                        class="text-indigo-400 font-medium">routine</span
                    > and consitency
                {:else}
                    Workouts specific to your <span
                        class="text-indigo-400 font-medium">environment</span
                    >
                    and
                    <span class="text-indigo-400 font-medium">expertise</span>
                {/if}
            </ProductCard>
        {/each}
    </div>
</SectionWrapper>
