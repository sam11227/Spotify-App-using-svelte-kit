<script>
  let count = 0;
  // let string = `you have clicled ${count} times`;

  $: string = `you have clciked ${count} times`

  
  $: if (count > 5){
    console.log(count, "update")
  }

  function increment(){
    count += 1;
  }
</script>
<button on:click={increment}>click {count}</button>
<h3>{string}</h3>


<style>
  button{
    padding: 15px 20px;
  }
</style>