<script>
  import Button from "./components/Button.svelte";

  let input = "";
</script>

<main
  class="fixed transition h-screen w-screen flex flex-col justify-center items-center bg-stone-300"
>
  <section
    class="bg-gray-200 shadow-lg p-5 inline-flex flex-col gap-5 rounded-3xl border-2 border-gray-100 max-w-sm"
  >
    <input
      class="rounded-2xl bg-gray-800 border-gray-900 border text-right text-white p-4 w-full text-4xl"
      type="text"
      name="input"
      id="input"
      value={input}
    />
    <div class="grid grid-cols-3 grid-rows-3 gap-4 max-w-md">
      {#each [7, 8, 9, 4, 5, 6, 1, 2, 3] as num}
        <Button number={num} on:press={(e) => (input += e.detail.text)} />
      {/each}
      <Button number={"X"} />
      <Button number={"-"} />
      <Button number={"+"} />
      <Button number={"."} />
    </div>
  </section>
</main>

<style global lang="postcss">
  @tailwind base;
  @tailwind components;
  @tailwind utilities;
</style>
