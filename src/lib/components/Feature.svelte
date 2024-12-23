<script lang="ts">
    export let descriptionPosition: "left" | "right" | "top";
    const descriptionStyle =
        "bg-blue-100 text-center max-w-xl shadow-lg p-6 rounded-2xl scroll-m-20 text-3xl font-medium tracking-tight transition-colors first:mt-0";
</script>

<div class="w-full">
    {#if descriptionPosition === "left"}
        <div class="flex flex-row w-full items-center justify-center gap-32">
            <h2 class={descriptionStyle}>
                <slot name="description" />
            </h2>
            <slot name="illustration" />
        </div>
    {:else if descriptionPosition === "right"}
        <div class="flex flex-row w-full items-center justify-center gap-32">
            <slot name="illustration" />
            <h2 class={descriptionStyle}>
                <slot name="description" />
            </h2>
        </div>
    {:else if descriptionPosition === "top"}
        <div class="flex flex-col w-full items-center justify-center gap-8">
            <h2 class={descriptionStyle}>
                <slot name="description" />
            </h2>
            <slot name="illustration" />
        </div>
    {/if}
</div>
