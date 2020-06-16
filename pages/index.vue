<template>
  <div>
    <div class="text-center mt-4">
      <b-button variant="primary">Adicionar postagem</b-button>
    </div>
    <h1 class="title">
      Últimas postagens
    </h1>
    <pre>{{ posts }}</pre>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: null
    }
  },
  async created() {
    this.posts = await this.$axios.$get('posts')
    console.log(this.image())
  }
}
</script>
