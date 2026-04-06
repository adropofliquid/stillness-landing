<!--
<script>
import Feature from "../components/Feature.svelte";
import WarehouseIcon from "../components/WarehouseIcon.svelte";
import ShoppingCartIcon from "../components/ShirtIcon.svelte";
import TimerIcon from "../components/LinkIcon.svelte";
import Faq from "../components/Faq.svelte";
import Icon from "@iconify/svelte";

    let faqs = [
        {
            question: "How do I upload my clothes to What2Wear?",
            answer: "Simply take clear photos of your clothes using your phone's camera. Open the app, navigate to the \"Wardrobe\" section, and follow the prompts to upload and categorize your items."
        },
        {
            question: "Can I edit or delete items from my virtual wardrobe?",
            answer: "Yes, you can easily manage your wardrobe. To edit or delete items, just select the item from your wardrobe list and choose the appropriate action from the options provided."
        },
        {
            question: "How does What2Wear suggest outfits?",
            answer: "What2Wear uses a simple pairing logic that matches tops and bottoms based on factors like color, style, and occasion. The app provides suggestions to help you quickly decide what to wear."
        },
        {
            question: "Is What2Wear available on both Android and iOS?",
            answer: "Yes, What2Wear is available for download on both Google Play and the Apple App Store. You can find the download links at the top of this page."
        },
        {
            question: "Is my data safe with What2Wear?",
            answer: "Absolutely! We take your privacy seriously. All images and data are securely stored, and we do not share your information with third parties."
        }
    ];

</script>

<div class="flex flex-col min-h-[100dvh]">
    <header class="px-4 lg:px-6  flex items-center pt-4">
        <a href="#" class="flex items-center justify-center">
            <img src="/logo.svg" class="h-16 w-16" />
            <span class="sr-only">What to Wear</span>
        </a>
        <nav class="ml-auto flex gap-4 sm:gap-6">
            <a href="https://blog.whattowearapp.com" class="text-sm font-medium hover:underline underline-offset-4">Blog</a>
            <a href="#features" class="text-sm font-medium hover:underline underline-offset-4">Features</a>
            <a href="#faq" class="text-sm font-medium hover:underline underline-offset-4">FAQ</a>
        </nav>
    </header>

    <section class="w-full py-12 md:py-24 lg:py-32">
            <div class="container mx-auto px-4 md:px-6">
                <div class="grid gap-6 lg:grid-cols-[1fr_500px] lg:gap-12 xl:grid-cols-[1fr_600px]">
                    <div class="flex flex-col justify-center space-y-4 mt-16">
                        <div class="space-y-4 mb-4">
                            <h1 class="text-center sm:text-start text-3xl font-bold tracking-tighter sm:text-5xl xl:text-6xl/none">
                                Quickly Decide What to Wear with Smart Suggestions
                            </h1>
                            <p class="text-center sm:text-start max-w-[600px] text-muted-foreground md:text-xl">
                                Tired of spending too much time choosing what to wear? Upload your wardrobe and let What2Wear suggest outfits that fit your style. Save time and feel confident every day with our easy-to-use app
                            </p>
                        </div>
                        <div class="flex mx-auto md:mx-0 gap-2 min-[400px]:flex-row">
                            <a href="https://apps.apple.com/app/w2w-what-2-wear/id6657955120" class="inline-flex h-10 items-center justify-center rounded-md bg-[#009688] px-8 text-sm font-medium text-primary-foreground shadow transition-colors hover:bg-primary/90 focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50">
                                <Icon icon="mingcute:appstore-fill" class="text-3xl mr-1"></Icon> App Store
                            </a>
                            <a href="https://play.google.com/store/apps/details?id=com.wsiw.whatshouldiwear" class="inline-flex h-10 items-center justify-center rounded-md border border-input bg-background px-8 text-sm font-medium shadow-sm transition-colors hover:bg-accent hover:text-accent-foreground focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50">
                                <Icon icon="mage:playstore" class="text-3xl mr-1"></Icon> Play Store
                            </a>
                        </div>
                    </div>
                    <div class="relative">
                        <img src="/wardrobe.png" alt="wardrobe" class="mx-auto object-cover sm:w-full lg:aspect-square" />
                        <div class="absolute inset-0 bg-gradient-to-t from-background to-transparent"></div>
                    </div>
                </div>
            </div>
        </section>

    <section id="features" class="w-full py-12 md:py-24 lg:py-32 bg-muted">
            <div class="container  mx-auto px-4 md:px-6">
                <div class="flex flex-col items-center justify-center space-y-4 text-center">
                    <div class="space-y-2">
                        <h2 class="text-3xl font-bold tracking-tighter sm:text-5xl">Discover How What2Wear Simplifies Your Style</h2>
                        <p class="max-w-[900px] text-muted-foreground md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed">
                            Explore our features that help you save time, look great, and feel confident every day.
                        </p>
                    </div>
                </div>

                <div class="mx-auto grid max-w-5xl items-center gap-6 py-12 lg:grid-cols-3 lg:gap-12">
                    <Feature title="Virtual Wardrobe" description="Easily upload and organize photos of your clothes. Access your entire wardrobe from your phone and keep track of your favorite pieces." icon={WarehouseIcon} />
                    <Feature title="Outfit Recommendations" description="Get instant outfit suggestions based on your uploaded wardrobe. What2Wear pairs tops and bottoms for a perfect match, tailored to your style.." icon={TimerIcon} />
                    <Feature title="Personalized Style Insights" description="Receive tips and insights based on your wardrobe and preferences. What2Wear learns your style over time, offering better suggestions with every use." icon={ShoppingCartIcon} />
                </div>
            </div>
        </section>
    <!-- Virtual Wardrobe Section -->
    <section class="py-16">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-8 md:mb-0 md:pl-8">
                    <h2 class="text-3xl sm:text-4xl font-bold mb-4 leading-tight">
                        Your Wardrobe, Digitized
                    </h2>
                    <p class="text-lg text-gray-700 sm:text-xl mb-6 leading-relaxed">
                        Easily catalog your clothes and accessories with What2Wear. Browse your virtual wardrobe anytime, and plan outfits with ease, all in one place.
                    </p>
                    <a href="#download" class="inline-flex h-10 items-center justify-center rounded-md bg-[#009688] px-8 text-sm font-medium text-white transition-colors hover:bg-[#00796B] focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-[#004D40]">
                        Learn More
                    </a>
                </div>
                <div class="md:w-1/2 relative">
                    <img src="/wardrobes.png" alt="wardrobe" class="rounded-lg w-3/4 mx-auto" />
                    <div class="absolute inset-0 mx-auto w-full h-full max-w-sm bg-gradient-radial from-[#E0F7FA] to-transparent opacity-70 -z-10"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- Recommendation System Section -->
    <section class="py-16 bg-gray-50">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row-reverse items-center">
                <div class="md:w-1/2 mb-8 md:mb-0 md:pl-8">
                    <h2 class="text-3xl font-bold mb-4">Style Recommendations</h2>
                    <p class="text-lg text-gray-700 sm:text-xl mb-6 leading-relaxed">
                        Let our smart algorithm analyze your wardrobe to suggest outfit combinations that match your style and suit any occasion.
                    </p>
                    <a href="#download" class="inline-flex h-10 items-center justify-center rounded-md bg-[#009688] px-8 text-sm font-medium text-primary-foreground shadow transition-colors hover:bg-primary/90 focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50">
                        Get Started
                    </a>
                </div>
                <div class="md:w-1/2">
                    <img src="/suggest.png" class="w-3/4 mx-auto"  alt="Recommendation System"/>
                </div>
            </div>
        </div>
    </section>


    <!-- FAQ Section -->
    <section id="faq" class="py-16">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12">Frequently Asked Questions</h2>
            <div class="max-w-3xl mx-auto">
                {#each faqs as faq}
                    <Faq question={faq.question} answer={faq.answer} />
                {/each}
            </div>
        </div>
    </section>

    <!-- Call to Action -->
    <section id="download" class="py-16 bg-[#009688] text-white">
        <div class="container mx-auto px-4 text-center">
            <h2 class="text-3xl font-bold mb-4">Ready to Elevate Your Style?</h2>
            <p class="text-xl mb-8">Download our app today and transform your wardrobe experience.</p>
            <div class="flex justify-center gap-4">
                <img src="/qr-code.png" alt="scan me"/>
            </div>
            <div class="flex justify-center gap-4 mt-8">
                <a href="https://apps.apple.com/app/w2w-what-2-wear/id6657955120" class="inline-flex h-12 items-center justify-center rounded-md bg-white text-[#009688] px-6 text-sm font-medium shadow transition-colors hover:bg-gray-100 focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50">
                    <Icon icon="mingcute:appstore-fill" class="text-3xl mr-1"></Icon> Download for iOS
                </a>
                <a href="https://play.google.com/store/apps/details?id=com.wsiw.whatshouldiwear" class="inline-flex h-12 items-center justify-center rounded-md bg-white text-[#009688] px-6 text-sm font-medium shadow transition-colors hover:bg-gray-100 focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50">
                    <Icon icon="mage:playstore" class="text-3xl mr-1"></Icon> Download for Android
                </a>
            </div>
        </div>
    </section>

    <footer class="flex flex-col gap-2 sm:flex-row py-6 w-full shrink-0 items-center px-4 md:px-6 border-t">
        <p class="text-xs text-muted-foreground">&copy; 2025 Stillness. All rights reserved.</p>
        <nav class="sm:ml-auto flex gap-4 sm:gap-6">
            <a href="/privacy" class="text-xs hover:underline underline-offset-4">Terms of Service</a>
            <a href="/privacy" class="text-xs hover:underline underline-offset-4">Privacy</a>
        </nav>
    </footer>
</div>
-->
