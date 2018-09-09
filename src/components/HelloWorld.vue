<template>
  <v-container fluid>
    <v-slide-y-transition mode="out-in">
      <v-layout column align-left>
        <div v-for="theme in themes" :key="theme">
          <h2>
            <span :class="theme">{{ theme }}</span>
            <span :class="theme+'--text'">The quick brown fox jumps over the lazy dog.</span>
          </h2>
        </div>
      </v-layout>
    </v-slide-y-transition>
  </v-container>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data () {
    return {
      themes: [
        'primary',
        'secondary',
        'accent',
        'error',
        'info',
        'success',
        'warning'
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
