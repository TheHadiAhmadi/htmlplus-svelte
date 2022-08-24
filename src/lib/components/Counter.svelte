<script>
  import "@htmlplus/core/counter";
  import { onMount } from "svelte";

  export let easing = 'ease-out-expo';

  export let decimal = '.';
  export let decimals = 0;


  export let delay = 0;
  export let duration = 1000;
  export let from = 0;
  export let play = false

  export let separator = undefined
  export let to = undefined


  export function complete() {
      ref.complete()
  }
  export function pause() {
      ref.pause()
  }
  export function start() {
      ref.start()
  }
  export function stop() {
      ref.stop()
  }
  
  
  let ref;

  onMount(() => {
    console.log(ref);
    ref.start()
  });

  $: console.log(ref)
</script>

<plus-counter bind:this={ref} {to} {delay} {duration} {easing} {decimal} {decimals} {from} {play} {separator}>
    <slot/>
</plus-counter>
