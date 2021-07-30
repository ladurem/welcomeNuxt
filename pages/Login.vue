<template>
  <body style="font-family:Roboto">
    <div
      class="w-full h-screen md:-mx-4"
      style="filter: blur(6px);"
    />
    <div class="absolute w-3/5 bg-white" style="transform: translate(-50%, -50%); top:50%; left:50%">
      <img class="border-0 rounded-full w-20 h-20 mx-auto" src="icon.png">

      <div class="px-12 py-10">
        <div class="md:flex">
          <br>Mon tet actif
        </div>
        <div class="w-full mb-2">
          <div class="flex items-center">
            <i class="ml-3 fill-current text-gray-400 text-xs z-10 far fa-user" />
            <input type="text" placeholder="username" class="-mx-6 px-8  w-full border rounded px-3 py-1 text-gray-700">
          </div>
        </div>
        <div class="w-full mb-2">
          <div class="flex items-center">
            <i class="ml-3 fill-current text-gray-400 text-xs z-10 fas fa-lock" />
            <input type="text" placeholder="password" class="-mx-6 px-8 w-full border rounded px-3 py-1 text-gray-700">
          </div>
        </div>
        <div class="mt-8 flex justify-between">
          <div class="flex items-center">
            <input id="checl" type="checkbox" class="w-4 h-4 mr-2">
            <label for="checl"><span class="text-xs text-gray-700">Remember Me</span></label>
          </div>
          <div>
            <NuxtLink to="/">
              <span type="text" class="bg-yellow-400 text-xs text-gray-700 rounded px-4 py-2">
                SIGN IN
              </span>
            </NuxtLink>
          </div>
        </div>
      </div>
    </div>
    </div>
  </body>
</template>

<script>
export default {
  name: 'Login'
}
</script>

<style scoped>

</style>
