<template>
  <nav
    class="flex items-center justify-between flex-wrap bg-gray-900 p-6 text-white"
  >
    <NuxtLink class="flex items-center flex-shrink-0 mr-6" to="/"
      ><span class="font-semibold text-xl tracking-tight"
        >Firengii</span
      ></NuxtLink
    >
    <div class="block lg:hidden">
      <button
        class="flex items-center px-3 py-2 border rounded text-teal-200 border-teal-400 hover:text-white hover:border-white"
        type="button"
      >
        <svg
          class="fill-current h-3 w-3"
          viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <title>Menu</title>
          <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
        </svg>
      </button>
    </div>

    <div
      class="w-full block flex-grow lg:flex lg:items-center lg:w-auto"
      id="navbarSupportedContent"
    >
      <div class="text-sm lg:flex-grow">
        <NuxtLink
          to="/products"
          class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4"
          >Products <span class="sr-only">(current)</span></NuxtLink
        >
        <NuxtLink
          to="/my-items"
          class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4"
          >My Items <span class="sr-only">(current)</span></NuxtLink
        >
      </div>
    </div>
  </nav>
</template>

<script>
export default {};
</script>
