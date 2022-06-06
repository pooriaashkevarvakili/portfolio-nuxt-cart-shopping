<template>
  <v-app>
    <v-row class="mt-3">


      <div class="col-md-4 col-lg-4 col-xs-12 col-sm-12 h-12">


        <v-card height="72%">
          <v-row justify="center">


            <v-img max-height="100" max-width="180" src="img9.jpg" style="width:230px;height:170px" alt="">
            </v-img>
          </v-row>


          <div class="black--text mt-16 ">
            <div class="ml-6">
              macbook Retina 13.3' ME662 (2013)
            </div>
            <div class="ml-6 mt-2">
              10 left in stock </div>
            <div class="ml-6 mt-3">
              2.9 Ghz Dual-Core Intel Core i5 Broadwell Tubro boost up to 3.3 GHz with L3 3MB cache</div>
          </div>
          <v-container>

            <v-row class="mt-10">
              <div class="black--text ml-5 ">
                $2399

              </div>
              <v-spacer />
              <v-btn :to="{ name: 'cart' }" class="mr-5 green">add to cart</v-btn>
            </v-row>
          </v-container>
        </v-card>
      </div>
      <div class=" col-md-4 col-lg-4 col-xs-12 col-sm-12">


        <v-card height="50%">
          <div>mohamad</div>
          <div>ali</div>
        </v-card>
      </div>
    </v-row>
  </v-app>

</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
<style>
.theme--dark.v-card {
  background-color: #fff;
  /* color: #FFFFFF; */
}
</style>