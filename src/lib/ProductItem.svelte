<script lang="ts">
  import FaCartPlus from "svelte-icons/fa/FaCartPlus.svelte";
  import FaRegEye from "svelte-icons/fa/FaRegEye.svelte";
  import FaHeart from "svelte-icons/fa/FaHeart.svelte";
  import FaStar from "svelte-icons/fa/FaStar.svelte";
  import type { Product } from "./types";

  export let handleAddToCard;
  export let handleAddWishList;
  export let handleLike;
  export let handleRate;

  const product: Product = {
    id: 6,
    title: "MacBook Pro",
    description:
      "MacBook Pro 2021 with mini-LED display may launch between September, November",
    price: 1749,
    discountPercentage: 11.02,
    rating: 4.57,
    stock: 83,
    brand: "APPle",
    category: "laptops",
    thumbnail: "https://i.dummyjson.com/data/products/6/thumbnail.png",
    images: [
      "https://i.dummyjson.com/data/products/6/1.png",
      "https://i.dummyjson.com/data/products/6/2.jpg",
      "https://i.dummyjson.com/data/products/6/3.png",
      "https://i.dummyjson.com/data/products/6/4.jpg",
    ],
  };
</script>

<div class="w-96">
  <div class="group/card relative w-full h-80 overflow-hidden">
    <img
      class="top-0 left-0 w-full h-full object-cover hover:scale-150 ease-in-out duration-500 origin-right"
      src={product.images[0]}
      alt={product.title}
    />
    <ul class="action absolute top-3 right-3">
      <li
        class="group flex justify-center items-center m-1 relative list-none bg-white w-10 h-10 p-3 cursor-pointer translate-x-16 duration-300 delay-75 hover:bg-red-500 hover:text-slate-50 hover:opacity-100 group-hover/card:translate-x-0"
        on:click={handleAddToCard}
      >
        <FaCartPlus />
        <span
          class="opacity-0 absolute right-[50px] -translate-x-[20px] bg-white text-gray-900 p-2 whitespace-nowrap pointer-events-none duration-500 group-hover:opacity-100 group-hover:translate-x-[0px]"
          >Add to cart</span
        >
      </li>
      <li
        class="group flex justify-center items-center m-1 relative list-none bg-white w-10 h-10 p-3 cursor-pointer translate-x-16 duration-300 delay-100 hover:bg-red-500 hover:text-slate-50 hover:opacity-100 group-hover/card:translate-x-0"
        on:click={handleAddWishList}
      >
        <FaRegEye />
        <span
          class="opacity-0 absolute right-[50px] -translate-x-[20px] bg-white text-gray-900 p-2 whitespace-nowrap pointer-events-none duration-500 group-hover:opacity-100 group-hover:translate-x-[0px]"
          >View details</span
        >
      </li>
      <li
        class="group flex justify-center items-center m-1 relative list-none bg-white w-10 h-10 p-3 cursor-pointer translate-x-16 duration-300 delay-150 hover:bg-red-500 hover:text-slate-50 hover:opacity-100 group-hover/card:translate-x-0"
        on:click={handleLike}
      >
        <FaHeart />
        <span
          class="opacity-0 absolute right-[50px] -translate-x-[20px] bg-white text-gray-900 p-2 whitespace-nowrap pointer-events-none duration-500 group-hover:opacity-100 group-hover:translate-x-[0px]"
          >Add to widh list</span
        >
      </li>
    </ul>
  </div>
  <div class="content">
    <h2 class="text-lg font-semibold text-slate-800 mt-2">
      {product.title} <br />
      <span class="" />
    </h2>
    <p class="" />
    <div class="price-rating flex justify-between items-center">
      <h2 class="text-red-600 text-xl font-semibold">{product.price}$</h2>
      <div class="rating flex flex-wrap" on:click={handleRate}>
        <span class="h-5 text-yellow-400 cursor-pointer">
          <FaStar />
        </span>
        <span class="h-5 text-yellow-400 cursor-pointer">
          <FaStar />
        </span>
        <span class="h-5 text-yellow-400 cursor-pointer">
          <FaStar />
        </span>
        <span class="h-5 text-yellow-400 cursor-pointer">
          <FaStar />
        </span>
        <span class="h-5 text-yellow-400 cursor-pointer">
          <FaStar />
        </span>
      </div>
    </div>
  </div>
</div>

<style>
</style>
