<script>
    export let size = "small";
    export let shadow = false;
</script>

<button
    class:size-lg={size == "large"}
    class:size-sm={size == "small"}
    class:shadow
>
    <slot>text</slot>
</button>

<style lang="scss">
    button {
        background-color: #ff3e00;
        color: #ffffff;
        border-radius: 30px;
        border: none;
        font-weight: bold;
        cursor: pointer;
        &:hover{
            background-image: linear-gradient(rgba(0,0,0,0.4)0 0);
        }
        &:active{
            background-image: linear-gradient(rgba(255, 255, 255, 0.1) 0 0);
        }
        &.size-sm {
            padding: 15px 20px;
        }
        &.size-lg {
            padding: 20px 25px;
            font-size: 20px;
        }
        &.shadow {
            box-shadow: 0 0 10px rgba(1, 1, 1, 0.3);
        }
    }
</style>
