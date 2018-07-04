<template>
 <div class="details">
  <div class="container">
   <div class="row">
    <div class="col-md-12" v-for="(shoe,index) in shoes" :key="index">
     <div v-if="shoeId == shoe.sid">
      <h1>{{shoe.shoeName}}</h1>
      <img :src="shoe.image" class="img-fluid">
     </div>
    </div>
   </div>
  </div>
 </div>
</template>
<script>
 export default{
  name:'details',
  data(){
   return{
    shoeId:this.$route.params.idd,
    title:"details",
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
  }
 }
</script>
