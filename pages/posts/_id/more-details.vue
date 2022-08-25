<template>
  <div>
    <h1>more details for: {{$route.params.id}}</h1>
  </div>
</template>

<script>
export default {
  validate (data) {
    // questo metodo viene eseguito all'arrivo in questa route con un parametro, 
    // il data rappresenta il payload, da li si potrà validare quello che si vuole.
    // il 'return' di questo metodo decreta se la validazione sia andata bene o meno, 
    // nel caso non sia un parametro corretto allora la pagina non verrà trovata
    return /^\d+$/.test(data.params.id) // in questo caso funzionerà solo con id numerici
  }
}
</script>