  <!-- SlotMachine.svelte -->
  <script>
    import { onMount, } from 'svelte';
    import { slide } from 'svelte/transition';

  const items = ["a travel companion", "a guided journal", "a keepsake"];
  let currentIndex = 0;

  function spin() {
    // Increment currentIndex
    currentIndex = (currentIndex + 1) % items.length;
  }

  onMount(() => {
    // Start spinning every 2 seconds
    const interval = setInterval(spin, 2000);

    return () => {
      clearInterval(interval);
    };
  });
</script>

<style>
  .slot-machine {
    position: relative;
    height: 1.5em; /* Adjust as needed */
    overflow: hidden;
  }

  .slot-machine span {
    position: absolute;
    left: 0;
    width: 100%;
    transition: transform 0.5s ease;
  }

  .slot-machine span.previous {
    transform: translateY(-100%);
  }
</style>

<div class="slot-machine">
  <span transition:slide class="current">{items[currentIndex]}</span>
  <span transition:slide class="previous">{items[(currentIndex - 1 + items.length) % items.length]}</span>
</div>