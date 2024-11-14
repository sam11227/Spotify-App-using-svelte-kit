<script>
    import Button from "./button.svelte";

    export let todos = [];
    let inputText;
    function handelAddTodo(){
        console.log(inputText)
    }
</script>

<div class="todo-list-wrapper">
    <ul>
        {#each todos as { id, title }, index (id)}
            {@const number = index + 1}
            <li>{number}-{title}</li>
        {/each}
    </ul>
    {inputText}
    <form class="add-todo-form" on:submit|preventDefault={handelAddTodo}>
        <!-- <input bind:this={input}/> -->
         <!-- <input on:input={(e) => {
            inputText = e.currentTarget.value
         }}/> -->
         <!-- in svelte for grt the value simple we get value like that for input -->
         <input bind:value={inputText}/>
        <Button type='submit'>Add</Button>
    </form>
</div>
