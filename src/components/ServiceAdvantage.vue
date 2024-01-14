<template>
  <div class="container service-advantage mt-4">
    <div class="row">
       <div class="col-xs-3 col-md-3 col-sm-6 text-center justify-center"
         v-for="item in items">
            <v-img
              class="mx-auto"
              :src="item.image"
              width="120" />
         <p class="f-18">{{item.text}}</p>
       </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ServiceAdvantage',
  data() {
    return {
      items: [
        {
          text: 'Large hearty portions',
          image: require('../assets/images/bread.png'),
        },
        {
          text: 'Free delivery every 2 days',
          image: require('../assets/images/map.png'),
        },
        {
          text: 'Fresh products, cooking in Yerevan',
          image: require('../assets/images/packet.png'),
        },
        {
          text: 'Just need a microwave',
          image: require('../assets/images/micro.png'),
        },
      ],
    };
  },
};
</script>
