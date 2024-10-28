<script>
    import Counter from "./lib/Counter.svelte";
    const maxCount = 10;
    const props ={
        color :10,
        Text : "working"
    }
</script>
<Counter initialCount={3} maxCount={maxCount} {...props}/>