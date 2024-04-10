<script>
  export default {
    data(){
      return {
        links:{
          women: 'Donna',
          men: 'Uomo',
          kids: 'Bambino'
        },

        chooses:{
          profile: 'Prof',
          favourites: 'Fav',
          cart: 'Cart'
        }
      }
    }
  }
</script>

<template>
  <header class="main-header">
    <div class="container">
      <div class="row">
        <div class="f-col">
          <ul class="links">
            <li v-for="(link, i) in links">
              <a href="#">{{link}}</a>
            </li>
            <!-- <li>
              <a href="#">Uomo</a>
            </li>
            <li>
              <a href="#">Bambini</a>
            </li> -->
          </ul>
        </div>
        <div class="s-col">
          <a href="#">
            <img class="logo" src="/public/img/Logo.png" alt="logo" />
            <h1 class="logo-title"><strong>Boolean</strong></h1>
          </a>
        </div>
        <div class="t-col">
          <ul class="links">
            <li v-for="(choose, i) in chooses">
              <a class="border" href="#">{{choose}}</a>
            </li>
            <!-- <li>
              <a class="border" href="#">Fav</a>
            </li>
            <li>
              <a class="border" href="#">Cart</a>
            </li> -->
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>


<style lang="scss" scoped>

  @use '../style/partials/header-section';

</style>