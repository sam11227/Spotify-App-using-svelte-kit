<script>
  let count1 = 0;
  let count2 = 0

  $: total = `you have click ${GetTotal(count1 , count2)} time`

  function Increment1(){
    count1 ++
  }
  function Increment2(){
    count2 --
  }

  function GetTotal(x , y){
    console.log(x,y)
    const yes = x - y
    console.log(yes,'yes')
   return yes
  }

</script>
<button on:click={Increment1}>click{count1}</button>
<button on:click={Increment2}>click{count2}</button>

<h3>{total}</h3>

<style>
  button{
    padding: 10px;
    color: black;
    background-color: aqua;
  }
  h3{
    color: red;
  }
</style>