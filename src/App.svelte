<script>
    import Counter from "./lib/Counter.svelte";
    import Button from "./lib/button.svelte";
    const maxCount = 10;
    const props ={
        color :10,
        Text : "working"
    }
</script>
<!-- <Counter initialCount={3} maxCount={maxCount} {...props}/>  -->
<Button size="small" shadow>Button Text</Button>