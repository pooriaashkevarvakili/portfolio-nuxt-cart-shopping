<template>
  <v-app>

    <v-app-bar fixed app>
      <router-link :to="{ name: 'index' }" class="white--text" style="cursor:pointer;text-decoration: none;">
        online store
      </router-link>


      <v-spacer />
      <router-link :to="{ name: 'login' }" class="white--text " style="cursor:pointer;text-decoration: none;">
        login
      </router-link>

      <v-btn class="ml-4 green" :to="{ name: 'cart' }" style="cursor:pointer">checkout</v-btn>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>


  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
<style >
.theme--dark.v-application {
  background: #fff;
  color: #FFFFFF;
}
</style>