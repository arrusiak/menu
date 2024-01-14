<template>
  <div class="position-absolute">
    <v-app-bar
      app
      color="white"
      dark
      class="header-bar justify-center"
    >
      <div class="col-12 d-flex align-center justify-center">
        <div class="desktop-menu">
          <router-link class="route-link" to="/FAQ">
            <span class="mr-2 black--text" @click="scrollToSection('faq')">FAQ</span>
          </router-link>
          <router-link class="route-link" to="/Delivery">
            <span class="mr-2 black--text" @click="scrollToSection('delivery')">Delivery</span>
          </router-link>
          <router-link class="route-link" to="/Menu">
            <span class="mr-2 black--text" @click="scrollToSection('menu')">Menu</span>
          </router-link>
        </div>
      </div>
      <div class="header-item-right-position row">
        <div class="desktop-phone col-8">
          <div class="text-right">
            <v-btn class="header-phone-icon ma-2" raunded>
              <v-icon
                color="darken-2"
              >
                mdi-phone
              </v-icon>
            </v-btn>
            <span class="text-14px">
                +374 (77) 77-77-77
              </span>
          </div>
          <div class="text-right" style="margin-top: -17px">
            <a href="tel:+37477777777" class="green-text text-right">Call me</a>
          </div>
        </div>
        <div class="col-1 mobile-column text-right">
          <v-btn rounded color="green-btn">ORDER</v-btn>
        </div>
        <div class="col-1">
          <v-btn icon @click="toggleBlock">
            <img src="../assets/images/menu_icon.png" alt="menu icon" class="menu-icon-mobile" />
          </v-btn>
        </div>
      </div>
    </v-app-bar>
    <div class="mobile-submenu" v-if="showBlock">
      <v-card>
        <v-list density="compact">
          <v-list-item
            v-for="(item, i) in items"
            :key="i"
            :value="item"
            color="primary"
          >
            <v-list-item-title v-text="item.text" @click="scrollToSection(item.scroll)"></v-list-item-title>
          </v-list-item>
        </v-list>
      </v-card>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'HeadBar',
    data() {
      return {
        items: [
          {
            text: 'FAQ',
            id: 1,
            scroll: 'faq'
          },
          {
            text: 'Delivery',
            id: 2,
            scroll: 'delivery'
          },
          {
            text: 'Menu',
            id: 3,
            scroll: 'menu'
          },
        ],
        showBlock: false,
      };
    },
    methods: {
      toggleBlock() {
        this.showBlock = !this.showBlock;
      },
      scrollToSection(ref) {
        this.$emit('scrollToSection', ref);
      },
    },
  };
</script>
