<template>
  <div class="container menu-container">
    <h2 class="container-title">Sample menu for the day</h2>
    <div class="row mt-xs-6 mt-md-6 mt-sm-3">
      <div class="col-xs-6 col-md-6 col-sm-12">
        <div class="row">
          <div class="col-12">
            <span v-for="day in weekdays">
              <v-btn
                outlined
                class="outlined-sm-btn"
              >
                {{day}}
              </v-btn>
            </span>
          </div>
        </div>
        <div class="row">
          <div class="col-12">
            <p class="ccal">3 meals,
            <span>
                1541 ccal
            </span>
            </p>
          </div>
        </div>
        <div class="row">
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
                :key=""
                v-slot="{ active, toggle }"
              >
                <v-card
                  :color="active ? undefined : ''"
                  class="ma-4"
                  height="366"
                  width="210"
                  @click="toggle"
                >
                  <v-img
                    class="mx-auto slide-img mt-2"
                    :src="item.image"
                  />
                  <p class="slide-text f-16 mt-3 ml-4">{{item.text}}</p>
                  <span class="font-color-gray f-16 ml-4">{{item.description}}</span>
                </v-card>
              </v-slide-item>
            </v-slide-group>
          </v-sheet>
          </div>
        </div>
      </div>
      <div class="col-xs-6 col-md-6 col-sm-12">
        <div class="row">
          <div class="col-12">
            <p class="bold-small-text ml-6">Duration</p>
          </div>
        </div>
        <div class="row">
          <div class="col-12 salary-btn-section">
            <v-btn
              outlined
              class="outlined-sm-btn"
            >
              test order
            </v-btn>
            <v-btn
              outlined
              class="outlined-sm-btn week-sale"
            >
              <p>2 weeks</p> <br/>
              <span class="mobile-display font-color-orange f-16">-26%</span>
            </v-btn>
            <v-btn
              outlined
              class="outlined-sm-btn daily-sale btn-padding position-relative"
            >
              <p>month</p> <br/>
              <span class="mobile-display font-color-orange f-16">-43%</span>
            </v-btn>
          </div>
        </div>
        <div class="row">
          <div class="col-12">
            <hr class="line">
          </div>
        </div>
        <div class="f-16 row font-weight-bold salary-description-section">
          <div class="col-6 small-text">
            <p>36 meals, 12 days</p>
            <p class="d-flex align-center"> Sale
              <img src="../assets/images/infoIcon.png" alt="info icon" class="ml-2" style="cursor: pointer"/>
            </p>
            <p class="d-flex align-center"> Delivery
              <img src="../assets/images/infoIcon.png" alt="info icon" class="ml-2" style="cursor: pointer"/>
            </p>
          </div>
          <div class="col-6 big-text">
            <p class="text-right">660 AMD for day</p>
            <p class="font-color-orange text-right">-2 040 AMD</p>
            <p class="text-right">0 AMD</p>
          </div>
        </div>
        <div class="row">
          <div class="col-12">
            <p class="bold-small-text">Your telephone number</p>
          </div>
        </div>
        <div class="row">
          <div class="col-12">
            <input placeholder="+374" class="gray-input mb-3"/>
            <span class="font-color-gray-black f-16">to clarify details of the order</span>
          </div>
        </div>
        <div class="row">
          <div class="col-12">
            <v-btn rounded block color="large-green-btn f-18 justify-lg-space-between">
              <span>Order</span>
              <span>12 989 AMD</span>
            </v-btn>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Menu',
  data() {
    return {
      weekdays: ['mon', 'tu', 'we', 'thu', 'fri', 'sat', 'sun' ],
      model: null,
      items: [
        {
          text: 'Title of meal',
          description: '180 g / 200 ccal',
          image: require('../assets/images/menuimg.png'),
        },
        {
          text: 'Title of meal',
          description: '180 g / 200 ccal',
          image: require('../assets/images/menuimg1.png'),
        },
        {
          text: 'Title of meal',
          description: '180 g / 200 ccal',
          image: require('../assets/images/menuimg2.png'),
        },
        {
          text: 'Title of meal',
          description: '180 g / 200 ccal',
          image: require('../assets/images/menuimg.png'),
        },
        {
          text: 'Title of meal',
          description: '180 g / 200 ccal',
          image: require('../assets/images/menuimg1.png'),
        },
        {
          text: 'Title of meal',
          description: '180 g / 200 ccal',
          image: require('../assets/images/menuimg2.png'),
        },
        {
          text: 'Title of meal',
          description: '180 g / 200 ccal',
          image: require('../assets/images/menuimg.png'),
        },
        {
          text: 'Title of meal',
          description: '180 g / 200 ccal',
          image: require('../assets/images/menuimg1.png'),
        },
      ],
    };
  },
};
</script>
