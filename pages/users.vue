<!-- 
  creando un componente route che ha lo stesso nome di una cartella contenente delle sotto routes,
  ed usando all'interno di esso come in questo caso nel template il nuxt-child, allora il router,
  al cambio della route, se si tratta di una rotta sottostante a questa, renderizzerà il componente relativo alla rotta al posto del nuxt-child
  difatti adesso il more-detail.vue se si inserisce un nuovo utente viene renderizzato sotto e non in un'altra pagina
 -->

<template>
  <div>
    <h1>Users</h1>
    <p>Elenco id utenti: (work in progress)</p>
    <br>
    <input v-model="newUserId" type="text">
    <button @click="insertNewUserId()">Inserisci nuovo utente</button>
    <nuxt-child/>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newUserId: '',
    };
  },
  methods: {
    insertNewUserId() {
      this.$router.push('/users/'+ this.newUserId + '/more-detail');
    }
  },
}
</script>