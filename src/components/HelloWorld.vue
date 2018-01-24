<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <img v-if="mostrar" src="../assets/logo.png">
    {{ mostrar }}
     <div v-if="mostrar">
        {{ msg }}
      </div>
   <button @click="toggleMostrar">Mostrar/Ocultar</button>
  </div>
</template>

<script>
export default {
  name: 'testcard',
  data() {
    return {
      msg: 'Welcome',
      mostrar: true,
    };
  },
  methods: {
    toggleMostrar() {
      this.mostrar = !this.mostrar;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
