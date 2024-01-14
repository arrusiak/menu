<template>
  <div class="delivery-container custom-container">
    <div class="container">
      <h2 class="container-title">Delivery Map</h2>
      <div class="row justify-center  mt-xs-6 mt-md-6 mt-sm-3 delivery-content">
        <div class="col-xl-8 col-md-8 col-sm-12 text-center">
          <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d195167.66663275042!2d44.32375498310815!3d40.15353600650971!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x406aa2dab8fc8b5b%3A0x3d1479ae87da526a!2z0JXRgNC10LLQsNC9!5e0!3m2!1sru!2sam!4v1705235294570!5m2!1sru!2sam" width="100%" height="560" style="border-radius:30px;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
        <div class="col-xl-4 col-md-4 col-sm-12">
          <v-card
            class="mx-auto delivery-card"
            max-width=""
          >
            <v-card-title>
              <p class="bold-small-text">Check the delivery price</p>
            </v-card-title>

            <v-card-text>
              <label for="streetInput" class="font-color-black">enter adress</label>
              <input placeholder="street,apt" class="gray-input mb-3 outlined-mid-input" id="streetInput"/>
            </v-card-text>

            <v-divider class="mx-4"></v-divider>

              <ul class="delivery-description font-weight-bold f-14">
                <li>Free delivery in Yerevan  within the concrete ring. We deliver on Mondays, Wednesdays and Fridays in any two-hour interval from 6 to 12.</li>
                <li>In the blue zone, the surcharge is 250 AMD per delivery.</li>
              </ul>
          </v-card>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Delivery',
};
</script>
