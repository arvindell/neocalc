<script>
  export let number;

  import { createEventDispatcher } from "svelte";

  const dispatch = createEventDispatcher();

  function onClick() {
    dispatch("press", {
      text: number,
    });
  }
</script>

<button
  class="transition aspect-square p-1 from-slate-400 to-slate-300 border-2 border-slate-400 bg-gradient-to-br rounded-full text-slate-900 text-4xl active:from-slate-500 active:to-slate-400 active:border-slate-500 shadow-sm"
  on:click={onClick}
>
  {number}
</button>
