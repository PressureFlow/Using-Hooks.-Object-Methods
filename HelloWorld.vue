<template>
  <div>
    <h2>HelloWorld</h2>
  </div>  
  <div>
    <h2>{{count}}</h2>
    <button @click="incrementCount">Counter</button>
  </div>
  <div>
    <input type="number" v-model="number1">
    <input type="number" v-model="number2">
    <h2>{{ sum }}</h2>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data: function() {
    return {
      count: 0,
      number1: 0,
      number2: 0
    }
  },
  props: {
    msg: String
  }, 
  computed: {
    sum() {
      return this.number1 + this.number2;
    }
  },
  methods: {
    incrementCount() {
      this.count++;
    }
  },
  created: function() {
    console.log('Created hook called');
  },
  updated: function() {
    console.log(this.count)
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
