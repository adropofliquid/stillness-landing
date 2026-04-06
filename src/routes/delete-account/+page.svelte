<script>
    let showSuccessPopup = false;

    function handleSubmit() {
        // Simulate successful submission
        showSuccessPopup = true;

        // Hide the success popup after 10 seconds
        setTimeout(() => {
            showSuccessPopup = false;
        }, 10000);
    }
</script>

<div class="bg-gray-100 flex justify-center items-center h-screen">
    <div class="bg-white shadow-md rounded-lg p-8 w-full max-w-md">
        <h1 class="text-2xl font-bold mb-4">Submit an Account Delete Request</h1>
        <form on:submit|preventDefault={handleSubmit}>
            <div class="mb-4">
                <label for="email" class="block text-gray-700 font-bold mb-2"
                >Email Address</label
                >
                <input
                        type="email"
                        id="email"
                        name="email"
                        class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                        placeholder="Enter your email address"
                        required
                />
            </div>
            <div class="mb-4">
                <label for="reason" class="block text-gray-700 font-bold mb-2"
                >Reason for Deletion</label
                >
                <textarea
                        id="reason"
                        name="reason"
                        class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                        placeholder="Explain why you want to delete your account"
                        required
                ></textarea>
            </div>
            <div class="flex justify-end">
                <button
                        type="submit"
                        class="bg-red-500 hover:bg-red-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline"
                >
                    Submit Request
                </button>
            </div>
        </form>
    </div>

    {#if showSuccessPopup}
        <div
                class="fixed top-0 left-0 w-full h-full flex items-center justify-center bg-black bg-opacity-50 transition-opacity duration-500 ease-in-out"
        >
            <div
                    class="bg-green-500 text-white px-8 py-4 rounded-lg shadow-md transition-transform duration-500 ease-in-out transform scale-100"
            >
                <p class="text-lg font-bold">Success!</p>
                <p>Your account delete request has been submitted.</p>
            </div>
        </div>
    {/if}
</div>