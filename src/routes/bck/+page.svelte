<script>
    import Feature from "../../components/Feature.svelte";
    import WarehouseIcon from "../../components/WarehouseIcon.svelte";
    import ShoppingCartIcon from "../../components/ShirtIcon.svelte";
    import TimerIcon from "../../components/LinkIcon.svelte";
    import Faq from "../../components/Faq.svelte";

    let faqs = [
        {
            question: "How does the app recommend outfits?",
            answer: "Our app uses advanced AI to analyze your wardrobe and suggest stylish combinations based on color, style, and occasion."
        },
        {
            question: "Can I share my outfits with friends?",
            answer: "Yes! You can easily share your favorite outfits or get feedback from friends within the app."
        },
        {
            question: "Is my wardrobe data secure?",
            answer: "We take your privacy seriously. All your wardrobe data is encrypted and stored securely on our servers."
        }
    ];
</script>

<!-- Hero section (as provided) -->

<!-- Features Section -->
<section class="py-16 bg-gray-50">
    <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-12">Key Features</h2>
        <div class="grid md:grid-cols-3 gap-8">
            <Feature icon={WarehouseIcon} title="Virtual Wardrobe">
                Digitize your closet and access your entire wardrobe anytime, anywhere.
            </Feature>
            <Feature icon={ShoppingCartIcon} title="Smart Recommendations">
                Get personalized outfit suggestions based on your style and preferences.
            </Feature>
            <Feature icon={TimerIcon} title="Outfit Planning">
                Plan your outfits in advance and save time in your daily routine.
            </Feature>
        </div>
    </div>
</section>

<!-- Virtual Wardrobe Section -->
<section class="py-16">
    <div class="container mx-auto px-4">
        <div class="flex flex-col md:flex-row items-center">
            <div class="md:w-1/2 mb-8 md:mb-0">
                <h2 class="text-3xl font-bold mb-4">Your Wardrobe, Digitized</h2>
                <p class="text-lg text-gray-600 mb-6">
                    Easily catalog your clothes and accessories. Our app creates a virtual representation of your wardrobe, making it simple to browse and plan outfits.
                </p>
                <a href="#" class="inline-flex h-10 items-center justify-center rounded-md bg-[#009688] px-8 text-sm font-medium text-primary-foreground shadow transition-colors hover:bg-primary/90 focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50">
                    Learn More
                </a>
            </div>
            <div class="md:w-1/2">
                <img src="/virtual-wardrobe.png" alt="Virtual Wardrobe" class="rounded-lg shadow-lg" />
            </div>
        </div>
    </div>
</section>

<!-- Recommendation System Section -->
<section class="py-16 bg-gray-50">
    <div class="container mx-auto px-4">
        <div class="flex flex-col md:flex-row-reverse items-center">
            <div class="md:w-1/2 mb-8 md:mb-0 md:pl-8">
                <h2 class="text-3xl font-bold mb-4">AI-Powered Style Recommendations</h2>
                <p class="text-lg text-gray-600 mb-6">
                    Our smart algorithm analyzes your wardrobe and style preferences to suggest perfect outfit combinations for any occasion.
                </p>
                <a href="#" class="inline-flex h-10 items-center justify-center rounded-md bg-[#009688] px-8 text-sm font-medium text-primary-foreground shadow transition-colors hover:bg-primary/90 focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50">
                    See How It Works
                </a>
            </div>
            <div class="md:w-1/2">
                <img src="/recommendation-system.png" alt="Recommendation System" class="rounded-lg shadow-lg" />
            </div>
        </div>
    </div>
</section>

<!-- FAQ Section -->
<section class="py-16">
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
<section class="py-16 bg-[#009688] text-white">
    <div class="container mx-auto px-4 text-center">
        <h2 class="text-3xl font-bold mb-4">Ready to Elevate Your Style?</h2>
        <p class="text-xl mb-8">Download our app today and transform your wardrobe experience.</p>
        <div class="flex justify-center gap-4">
            <a href="#" class="inline-flex h-12 items-center justify-center rounded-md bg-white text-[#009688] px-8 text-sm font-medium shadow transition-colors hover:bg-gray-100 focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50">
                Download for iOS
            </a>
            <a href="#" class="inline-flex h-12 items-center justify-center rounded-md bg-white text-[#009688] px-8 text-sm font-medium shadow transition-colors hover:bg-gray-100 focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50">
                Download for Android
            </a>
        </div>
    </div>
</section>

<!-- Footer -->
<footer class="py-8 bg-gray-100">
    <div class="container mx-auto px-4">
        <div class="flex flex-col md:flex-row justify-between items-center">
            <div class="mb-4 md:mb-0">
                <img src="/icon.png" alt="What to Wear Logo" class="h-12 w-12" />
            </div>
            <nav class="flex gap-4">
                <a href="#" class="text-sm text-gray-600 hover:text-gray-900">Privacy Policy</a>
                <a href="#" class="text-sm text-gray-600 hover:text-gray-900">Terms of Service</a>
                <a href="#" class="text-sm text-gray-600 hover:text-gray-900">Contact Us</a>
            </nav>
            <div class="mt-4 md:mt-0">
                <p class="text-sm text-gray-600">&copy; 2024 What to Wear. All rights reserved.</p>
            </div>
        </div>
    </div>
</footer>