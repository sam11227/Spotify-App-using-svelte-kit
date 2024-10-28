<script>
  export let initialCount;
  export let maxCount = undefined;
  export let color;
  export let Text;

  console.log($$props ,$$restProps)

  let count1 = initialCount;

  // $: total = `you have click ${GetTotal(count1 , count2)} time`

  function Increment() {
    if (count1 == maxCount) return;
    count1++;
  }
  // function Increment2(){
  //   count2 --
  // }

  // function GetTotal(x , y){
  //   console.log(x,y)
  //   const yes = x - y
  //   console.log(yes,'yes')
  //  return yes
  // }
</script>

<button on:click={Increment}>click{count1}</button>
<h3>{color}</h3>
<h4>{Text}</h4>

<!-- <button on:click={Increment2}>click{count2}</button> -->

<!-- <h3>{total}</h3> -->

<style>
  button {
    padding: 10px;
    color: black;
    background-color: aqua;
  }
  h3 {
    color: red;
  }
</style>
