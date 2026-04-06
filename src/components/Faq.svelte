<script>
    export let question = '';
    export let answer = '';

    let isOpen = false;

    function toggleOpen() {
        isOpen = !isOpen;
    }
</script>

<div class="border-b border-gray-200">
    <button
            on:click={toggleOpen}
            class="flex w-full justify-between py-4 text-left text-lg font-medium focus:outline-none"
    >
        <span>{question}</span>
        <svg
                class={`h-6 w-6 transform transition-transform duration-200 ${
        isOpen ? 'rotate-180' : ''
      }`}
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
        >
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
        </svg>
    </button>
    {#if isOpen}
        <div class="pb-4 pt-2 ">
            <p class="text-gray-600">{answer}</p>
        </div>
    {/if}
</div>

<style>
    /* Add any additional styles here if needed */
</style>