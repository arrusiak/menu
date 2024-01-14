<template>
  <div class="custom-container">
    <div class="container">
      <h2 class="container-title">Testimonlials</h2>
      <div class="row justify-center  mt-xs-6 mt-md-6 mt-sm-3 delivery-content">
        <div class="col-12">
          <v-sheet>
              <v-slide-group
                v-model="model"
                class=""
                active-class="success"
                onscroll=""
              >
                <v-slide-item
                  v-for="item in items"
                  v-slot="{ active, toggle }"
                >
                  <v-card
                    class="ma-4 pa-3"
                    @click="toggle"
                  >
                    <span class="font-color-gray f-14 ma-8">{{item.date}}</span>
                    <v-img
                      class="mx-auto slide-img mt-2"
                      :src="item.image"
                    />
                  </v-card>
                </v-slide-item>
              </v-slide-group>
          </v-sheet>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Testimonlial',
  data() {
    return {
      items: [
        {
          date: '01.01.2023',
          image: require('../assets/images/menuimg.png'),
        },
        {
          date: '01.01.2024',
          image: require('../assets/images/menuimg1.png'),
        },
        {
          date: '01.01.2022',
          image: require('../assets/images/menuimg2.png'),
        },
        {
          date: '01.01.2024',
          image: require('../assets/images/menuimg.png'),
        },
        {
          date: '01.01.2024',
          image: require('../assets/images/menuimg1.png'),
        },
        {
          date: '01.01.2024',
          image: require('../assets/images/menuimg2.png'),
        },
        {
          date: '01.01.2024',
          image: require('../assets/images/menuimg.png'),
        },
        {
          date: '01.01.2024',
          image: require('../assets/images/menuimg1.png'),
        }
      ],
      model: null,
    }
  }
};
</script>
