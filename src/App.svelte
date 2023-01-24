<script lang="ts">
  import ProductItem from "./lib/ProductItem.svelte";
</script>

<main
  class="flex flex-col justify-center items-center h-screen w-screen bg-gray-100"
>
  <div class="text-center mb-10">
    <h1 class="text-2xl">Yet another product card</h1>
    <h2 class="text-lg">Made with Vite + Svelte and Tailwindcss in TS</h2>
  </div>
  <ProductItem
    handleAddToCard={() => {
      alert("handleAddToCard callback");
    }}
    handleAddWishList={() => {
      alert("handleAddWishList callback");
    }}
    handleLike={() => {
      alert("handleLike callback");
    }}
    handleRate={() => {
      alert("handleRate callback");
    }}
  />
</main>

<style>
</style>
