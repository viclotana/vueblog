<template>
 <div class='home'>
  <h1 class="text-primary text-center">{{title}}</h1>
  <div class="row">
      <div class="col-md-4 col-lg4" v-for="(data,index) in shoes" :key="index">
        <img :src="data.image" class="img-fluid">
         <h3 @click="showDetails(data.sid)">{{data.shoeName}}</h3>
      </div>
    </div>
 </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      title: 'Yeezy 350 Products',
      shoes: [
        {
          shoeName: 'Solar Red',
          image: require('../assets/yeezy1.jpg'),
          sid: 1
        },
        {
          shoeName: 'Black Red',
          image: require('../assets/yeezy2.jpg'),
          sid: 2
        },
        {
          shoeName: 'Frozen Yellow',
          image: require('../assets/yeezy3.jpg'),
          sid: 3
        },
        {
          shoeName: 'Zebra V2',
          image: require('../assets/yeezy4.jpg'),
          sid: 4
        },
        {
          shoeName: 'Beluga Grey',
          image: require('../assets/yeezy5.jpg'),
          sid: 5
        },
        {
          shoeName: 'Black Green',
          image: require('../assets/yeezy6.jpg'),
          sid: 6
        }
      ]
    }
  },
  methods: {
    showDetails: function (sheewId) {
      let shoeId = sheewId
      this.$router.push({name: 'details', params: {idd: shoeId}})
    }
  }
}
</script>
<style scoped>
.row img{
  max-height: 15em;
  width: 100%;
}
.row h3{
  cursor:pointer;
}
</style>
