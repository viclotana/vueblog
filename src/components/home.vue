<template>
 <div class="home">
  <h1>{{title}}</h1>
 </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      title: 'home',
      shoes: [
        {
          shoeName: "Solar Red",
          image: require('../assets/yeezy1.jpg'),
          shoeId: 1
        },
        {
          shoeName: "Black Red",
          image: require('../assets/yeezy2.jpg'),
          shoeId: 2
        },
        {
          shoeName: "Frozen Yellow",
          image: require('../assets/yeezy3.jpg'),
          shoeId: 3
        },
        {
          shoeName: "Zebra V2",
          image: require('../assets/yeezy4.jpg'),
          shoeId: 4
        },
        {
          shoeName: "Beluga Grey",
          image: require('../assets/yeezy5.jpg'),
          shoeId: 5
        }
      ]
    }
  }
}
</script>
<style scoped>
</style>
