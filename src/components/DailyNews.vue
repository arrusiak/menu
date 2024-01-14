<template>
  <div class="container">
    <img src="../assets/images/delicious.png" alt="delicious meal" class="position-absolute meal-img z-index" />
    <img src="../assets/images/delicious1.png" alt="delicious1 meal" class="position-absolute meal-img1 z-index" />
    <img src="../assets/images/delicious2.png" alt="delicious1 meal" class="position-absolute meal-img2 z-index"/>
    <img src="../assets/images/Star1.png" alt="Star Image" class="position-absolute star-img"/>
    <img src="../assets/images/Star2.png" alt="Star Image" class="position-absolute star1-img"/>
    <div class="row justify-center">
      <div class="col-6 text-center">
        <h1>Delicious breakfast,
          lunch and dinner
          <span class="text-light-green">499 AMD</span>
          <span class="discount">660 AMD</span>
        </h1>
      </div>
    </div>
    <div class="row">
      <div class="col-12 text-center">
        <p class="daily-description"> for 3 meals a day</p>
      </div>
    </div>
    <div class="row">
      <div class="col-12 text-center">
        <v-btn rounded class="white-btn">ORDER NOW</v-btn>
      </div>
    </div>
    <div class="row">
      <div class="col-12 text-right">
        <v-btn rounded class="light-orange-btn">The offe indeed<span class="f-27">12:31:12</span></v-btn>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DailyNews',
};
</script>
