<script>
    import { onMount } from 'svelte';
    import Icon from '@iconify/svelte';

    export let openModal;

    let email = '';
    let isSubmitting = false;
    let submitStatus = null; // null: not submitted, 'success', or 'error'

    async function addWaitlist(event) {
        event.preventDefault();
        isSubmitting = true;
        submitStatus = null;

        try {
            const response = await fetch('https://api.fashiondecider.com/waitlist', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({ email }),
            });

            if (response.ok) {
                submitStatus = 'success';
                setTimeout(() => {
                    openModal();
                }, 2000);
            } else {
                submitStatus = 'error';
            }
        } catch (error) {
            console.error('Error submitting form:', error);
            submitStatus = 'error';
        } finally {
            isSubmitting = false;
        }
    }

    onMount(() => {
        // Add any necessary initialization logic here
    });
</script>

<div class="flex bg-gray-500 bg-opacity-75 overflow-y-auto overflow-x-hidden fixed top-0 right-0 left-0 z-50 justify-center items-center w-full md:inset-0 max-h-full">
    <div class="relative p-4 w-full max-w-md">
        <div class="relative bg-white rounded-lg shadow">
            <div class="flex items-center justify-between p-4 md:p-5 border-b rounded-t">
                <h3 class="text-xl font-semibold text-gray-900">
                    Join our waitlist
                </h3>
                <button on:click={openModal} type="button" class="end-2.5 text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm w-8 h-8 ms-auto inline-flex justify-center items-center" data-modal-hide="authentication-modal">
                    <Icon icon="mdi:close" width="24" height="24" />
                    <span class="sr-only">Close modal</span>
                </button>
            </div>
            <div class="p-4 md:p-5">
                {#if submitStatus === 'success'}
                    <div class="flex flex-col items-center justify-center pb-8">
                        <Icon icon="mdi:check-circle" class="text-green-500" width="64" height="64" />
                        <p class="mt-4 text-lg font-semibold">Successfully added to waitlist!</p>
                    </div>
                {:else if submitStatus === 'error'}
                    <div class="flex flex-col items-center justify-center pb-8">
                        <Icon icon="mdi:close-circle" class="text-red-500" width="64" height="64" />
                        <p class="mt-4 text-lg font-semibold">Failed to add to waitlist. Please try again.</p>
                    </div>
                {:else}
                    <form on:submit|preventDefault={addWaitlist}>
                        <div class="pt-2 pb-8">
                            <p>Be the first to know when we are on App Store</p>
                        </div>
                        <div class="pb-4">
                            <input type="email" bind:value={email} name="email" id="email" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5" placeholder="name@email.com" required />
                        </div>
                        <button type="submit" class="w-full text-white bg-[#009688] text-primary-foreground focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 mb-4 text-center" disabled={isSubmitting}>
                            {#if isSubmitting}
                                <Icon icon="mdi:loading" class="animate-spin inline-block mr-2" />
                                Submitting...
                            {:else}
                                Join Now
                            {/if}
                        </button>
                    </form>
                {/if}
            </div>
        </div>
    </div>
</div>
