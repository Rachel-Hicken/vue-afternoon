<template>
  <div id="app">
    <header>
      <h1>Create</h1>
      <h1>Battle Bots</h1>
      <h1>Collection</h1>
    </header>
    <create :submit-new-bot="submitNewBot"/>
    <p>{{bots}}</p>
  </div>
</template>

<script>
import Create from './components/Create.vue'

export default {
  name: "app",
  data() {
    return {
      id:0,
      botName: '',
      attackValue: 0,
      healthValue: 0,
      bots: []
    };
  },
  methods:{
    submitNewBot(){
      this.id++;
      let newBot = {
      id: this.id,
      botName: this.botName,
      attackValue: this.attackValue,
      healthValue: this.healthValue
      }
      this.bots.push(newBot);
      // this.newBot = '';
      // this.attackValue = 0;
      // this.healthValue = 0;
    }
  },
  components: {
    create: Create
  }
};
</script>

<style scoped>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}
header{
  display: flex;
  justify-content: space-between;
  background: #15687a;
}

h1,
h2 {
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
