<template>
  <span>
    <toolbar />
    <p v-if="$fetchState.pending">
      Fetching mountains...
    </p>
    <p v-else-if="$fetchState.error">
      An error occurred :(
    </p>
    <div v-else>
      <h1>Nuxt Mountains</h1>
      <ul>
        <li v-for="mountain of mountains" :key="mountain.title">
          <div class="md:flex pb-5">
            <div class="md:flex-shrink-0">
              <img :src="mountain.image" :width="150" alt="" class="rounded-lg md:h-20">
            </div>
            <div class="uppercase tracking-wide text-sm text-blue-400 font-bold">{{ mountain.title }}</div>
            <span class="md:flex-shrink-0 mt-5 ml-10 text-gray-600">{{ mountain.description }}</span>
          </div>
        </li>
      </ul>
      <button @click="$fetch">
        Refresh
      </button>
    </div>
    <Chat />
  </span>
</template>

<script>
export default {
  data () {
    return {
      mountains: []
    }
  },
  async fetch () {
    this.mountains = await fetch(
      'https://api.nuxtjs.dev/mountains'
    ).then(res => res.json())
  },
  head: {
    title: 'Page d\'accueil',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'Description de la page d\'accueil'
      }
    ]
  },
  mounted () {
    this.$nextTick(() => {
      this.$nuxt.$loading.start()
      setTimeout(() => this.$nuxt.$loading.finish(), 500)
    })
  },
  activated () {
    // appeller fetch de nouveau si le dernier appel date de plus de 30 secondes
    if (this.$fetchState.timestamp <= Date.now() - 30000) {
      this.$fetch()
    }
  }
}
</script>
