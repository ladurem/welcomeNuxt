<template>
  <nav class="relative flex flex-wrap items-center justify-between px-2 py-3 bg-blue-600 mb-3">
    <div class="container px-4 mx-auto flex flex-wrap items-center justify-between">
      <div class="w-full relative flex justify-between lg:w-auto  px-4 lg:static lg:block lg:justify-start">
        <NuxtLink
          to="/"
          class="text-sm font-bold leading-relaxed inline-block mr-4 py-2 whitespace-nowrap uppercase text-white"
        >
          pink Color
        </NuxtLink>
        <button
          class="cursor-pointer text-xl leading-none px-3 py-1 border border-solid border-transparent rounded bg-transparent block lg:hidden outline-none focus:outline-none"
          type="button"
        >
          <span class="block relative w-6 h-px rounded-sm bg-white"/>
          <span class="block relative w-6 h-px rounded-sm bg-white mt-1"/>
          <span class="block relative w-6 h-px rounded-sm bg-white mt-1"/>
        </button>
      </div>
      <div id="example-navbar-warning" class="lg:flex flex-grow items-center">
        <ul class="flex flex-col lg:flex-row list-none ml-auto">
          <li class="nav-item">
            <NuxtLink
              to="/News"
              class="px-3 py-2 flex items-center text-xs uppercase font-bold leading-snug text-white hover:opacity-75"
              href="#pablo"
            >
              Discover
            </NuxtLink>
          </li>
          <li class="nav-item">
            <a
              class="px-3 py-2 flex items-center text-xs uppercase font-bold leading-snug text-white hover:opacity-75"
              href="#pablo"
            >
              Profile
            </a>
          </li>
          <li class="nav-item">
            <NuxtLink
              class="px-3 py-2 flex items-center text-xs uppercase font-bold leading-snug text-white hover:opacity-75"
              href="#pablo"
              to="/Login"
            >
              Setting
            </NuxtLink>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Toolbar'
}
</script>

<style scoped>

</style>
