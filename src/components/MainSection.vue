<script>
import CardsComponent from "./CardsComponent.vue";
import {store} from '../store.js';
import axios from 'axios';

export default {
  components: {
    CardsComponent,
  },

  data() {
    return {
      product: store.data
    };
  },
  
  mounted(){
      axios.get('http://localhost:3000/products').then((res) =>{
        
        console.log('questo è il parametro, con i suoi valori (tra cui DATA): ', res)

        for(let i = 0; i < res.data.length; i++){

          const data = res.data[i]

          this.product.push(data)
          
        }

      })
    }
};
</script>

<template>
  <main>
    <section>
      <div class="container">
        <div class="row">
          <!-- First Card -->
          <li class="column" v-for="(item, i) in product" :key="item.id" >
            <CardsComponent :item="item" />
          </li>

          <!-- Second Card -->
          <!-- <div class="column">
            <div class="card">
              <div class="card-content">
                <img class="card-img" src="/public/img/2.webp" alt="model 2" />
                <ul>
                  <li>
                    <span class="discount">-30%</span>
                  </li>
                  <li>
                    <span class="b-heart">&hearts;</span>
                  </li>
                </ul>
                <div class="card-hover">
                  <img src="/public/img/2b.webp" alt="model 2 hover" />
                  <span class="r-heart">&hearts;</span>
                </div>
              </div>
              <div class="card-description">
                <ul>
                  <li>
                    <p class="brand">Guess</p>
                  </li>
                  <li>
                    <h5 class="product">ROSES TEE</h5>
                  </li>
                  <li>
                    <p class="price">
                      20,99€ <span class="price-cout">29,99€</span>
                    </p>
                  </li>
                </ul>
              </div>
            </div>
          </div> -->

          <!-- Third Card -->
          <!-- <div class="column">
            <div class="card">
              <div class="card-content">
                <img class="card-img" src="/public/img/3.webp" alt="model 3" />
                <ul>
                  <li>
                    <span class="discount">-30%</span>
                  </li>
                  <li>
                    <span class="b-heart">&hearts;</span>
                  </li>
                </ul>
                <div class="card-hover">
                  <img src="/public/img/3b.webp" alt="model 3 hover" />
                  <span class="r-heart">&hearts;</span>
                </div>
              </div>
              <div class="card-description">
                <ul>
                  <li>
                    <p class="brand">Come Zucchero Filato</p>
                  </li>
                  <li>
                    <h5 class="product">VOGLIA DI COLORI PASTELLO</h5>
                  </li>
                  <li>
                    <p class="price">
                      129,99€ <span class="price-cout">184,99€</span>
                    </p>
                  </li>
                </ul>
              </div>
            </div>
          </div> -->

          <!-- Fourth Card -->
          <!-- <div class="column">
            <div class="card">
              <div class="card-content">
                <img class="card-img" src="/public/img/4.webp" alt="model 4" />
                <ul>
                  <li>
                    <span class="discount">-50%</span>
                  </li>
                  <li>
                    <span class="sustain">Sostenibilità</span>
                  </li>
                  <li>
                    <span class="b-heart">&hearts;</span>
                  </li>
                </ul>
                <div class="card-hover">
                  <img src="/public/img/4b.webp" alt="model 4 hover" />
                  <span class="r-heart">&hearts;</span>
                </div>
              </div>
              <div class="card-description">
                <ul>
                  <li>
                    <p class="brand">Levi's</p>
                  </li>
                  <li>
                    <h5 class="product">TEE UNISEX</h5>
                  </li>
                  <li>
                    <p class="price">
                      14,99€ <span class="price-cout">29,99€</span>
                    </p>
                  </li>
                </ul>
              </div>
            </div>
          </div> -->

          <!-- Fifth Card -->
          <!-- <div class="column">
            <div class="card">
              <div class="card-content">
                <img class="card-img" src="/public/img/5.webp" alt="model 5" />
                <ul>
                  <li>
                    <span class="b-heart">&hearts;</span>
                  </li>
                </ul>
                <div class="card-hover">
                  <img src="/public/img/5b.webp" alt="model 5 hover" />
                  <span class="r-heart">&hearts;</span>
                </div>
              </div>
              <div class="card-description">
                <ul>
                  <li>
                    <p class="brand">Maya Deluxe</p>
                  </li>
                  <li>
                    <h5 class="product">STRIP BODICE</h5>
                  </li>
                  <li>
                    <p class="price">99,99€</p>
                  </li>
                </ul>
              </div>
            </div>
          </div> -->

          <!-- Sixth Card -->
          <!-- <div class="column">
            <div class="card">
              <div class="card-content">
                <img class="card-img" src="/public/img/6.webp" alt="model 6" />

                <ul>
                  <li>
                    <span class="sustain new">Sostenibilità</span>
                  </li>
                  <li>
                    <span class="b-heart">&hearts;</span>
                  </li>
                </ul>
                <div class="card-hover">
                  <img src="/public/img/6b.webp" alt="model 6 hover" />
                  <span class="r-heart">&hearts;</span>
                </div>
              </div>
              <div class="card-description">
                <ul>
                  <li>
                    <span class="brand">Esprit</span>
                  </li>
                  <li>
                    <h5 class="product">MAGLIONE - BLACK</h5>
                  </li>
                  <li>
                    <span class="price">29,99€</span>
                  </li>
                </ul>
              </div>
            </div>
          </div> -->
        </div>
      </div>
    </section>
  </main>
</template>

<style lang="scss" scoped>
@use "../style/partials/main-section";
</style>
