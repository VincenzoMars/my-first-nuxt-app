<!-- 
  creando un componente route che ha lo stesso nome di una cartella contenente delle sotto routes,
  ed usando all'interno di esso come in questo caso nel template il nuxt-child, allora il router,
  al cambio della route, se si tratta di una rotta sottostante a questa, renderizzerà il componente relativo alla rotta al posto del nuxt-child
  difatti adesso il more-detail.vue se si inserisce un nuovo utente viene renderizzato sotto e non in un'altra pagina
 -->

<template>
  <div>
    <h1>Posts</h1>
    <p>Elenco posts ids: (work in progress)</p>
    <br>
    <input v-model="newPostsId" type="text">
    <button @click="generateNewPostId()">Inserisci nuovo utente</button>
    <nuxt-child/>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newPostsId: '',
    };
  },
  methods: {
    generateNewPostId() {
      this.$router.push('/posts/'+ this.newPostsId + '/more-details');
    }
  }
}
</script>