<script>
    import Counter from "./lib/Counter.svelte";
    import Button from "./lib/button.svelte";
    import { FaAngellist } from "svelte-icons/fa";
    import FaAllergies from "svelte-icons/fa/FaAllergies.svelte";

    const maxCount = 10;
    const props = {
        color: 10,
        Text: "working",
    };
</script>

<!-- <Counter initialCount={3} maxCount={maxCount} {...props}/>  -->
<Button  size="small" shadow bgColor="red" textColor="white">
    <div style:width="20px" slot="leftContent" let:isLeftHovered>
        {#if isLeftHovered}
            <FaAngellist />
        {:else}
            <FaAllergies />
        {/if}
    </div>
    Text</Button
>
