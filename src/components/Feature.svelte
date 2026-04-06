<script>
    export let title;
    export let description;
    export let icon;
</script>

<div class="flex flex-col items-center justify-center space-y-4 text-center">
    <div class="rounded-full bg-[#009688] p-4 text-primary-foreground">
        {#if icon}
            <svelte:component this={icon} class="h-8 w-8" />
        {/if}
    </div>
    <h3 class="text-xl font-bold">{title}</h3>
    <p class="text-muted-foreground">{description}</p>
</div>
