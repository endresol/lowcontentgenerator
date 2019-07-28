<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <input 
      type="text"
      name="api_key"
      v-model="apikey"
      placeholder="api key"
    />
    <br>
    <input 
      type="text"
      name="client_id"
      v-model="clientid"
      placeholder="client id"
    />
    <br>
    <button @click="authorize">Authorize</button>
    <button>Logout</button>
    <button>Generate slides</button>
    <br>
    <label id="status">{{status}}</label>
  </div>
</template>

<script>
import SlidesApi from '@/services/SlidesApi';

export default {
  name: 'SlideGenerator',
  props: {
    msg: String
  },
  data () {
    return {
      status: 'let\'s start!',
      apikey: '',
      clientid:'',
    }
  },
  methods: {
     authorize () {
      /* const response = await SlidesApi.authorize({
        key: this.apikey,
        id: this.clientid,
      }) */
      SlidesApi.authenticate(this.apikey, this.clientid);
    },
  },
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
