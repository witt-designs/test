<template>
  <div class="container mx-auto text-center py-16 px-6">

   <div v-if="$store.state.user">

    <br></br>

   <img src="../assets/placeholder_logo.png" class="front_image">
 

      <h1 class="title text-white">
        Plata 2.0
      </h1>
      <br></br>
      <h2 class="subtitle">
        Welcome!!! you are logged in to the home screen
      </h2>


      <nuxt-link
            to="/account"
            class="button--green "
          >
          Login
          </nuxt-link>

          <nuxt-link
            to="/about"
            class="button--grey "
          >
          About
          </nuxt-link>

      </div>

    <div v-if="!$store.state.user">

    <br></br>



   <img src="../assets/placeholder_logo.png" class="front_image">



      <h1 class="title text-white">
        Plata 2.0
      </h1>
      <br></br>
      <h2 class="subtitle">
        An Ethereum-based platform for exchanging digital assets
      </h2>

      <nuxt-link
            to="/login"
            class="button--green "
          >
          Login
          </nuxt-link>

          <nuxt-link
            to="/register"
            class="button--grey "
          >
          Register
          </nuxt-link>
      </div>

   
    </div>
  </div>
  </div>

</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
  }
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;

}
*/


.title {
  font-family: sans-serif;
  display: block;
  font-weight: 300;
  font-size: 50px;
  color: white;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 35px;
  text-allign: center;
  color: white;
  word-spacing: 5px;
  padding-bottom: 15px;

}

.links {
  padding-top: 15px;
}

.front_image {
  width: 300px;
}


</style>
