<script>
import CardsComponent from "./CardsComponent.vue";

export default {
  components: {
    CardsComponent,
  },

  data() {
    return {
      products: [
        {
          id: 1,
          frontImage: "1.webp",
          backImage: "1b.webp",
          brand: "Levi's",
          name: "Relaxed Fit",
          price: 29.99,
          isInFavorites: true,
          badges: [
            {
              type: "tag",
              value: "Sostenibilità",
            },
            {
              type: "discount",
              value: "-50%",
            },
          ],
        },
        {
          id: 2,
          frontImage: "2.webp",
          backImage: "2b.webp",
          brand: "Guess",
          name: "Roses Tee",
          price: 20.99,
          isInFavorites: true,
          badges: [
            {
              type: "discount",
              value: "-30%",
            },
          ],
        },
        {
          id: 3,
          frontImage: "3.webp",
          backImage: "3b.webp",
          brand: "Come Zucchero Filato",
          name: "Voglia di colori pastello",
          price: 129.99,
          isInFavorites: false,
          badges: [
            {
              type: "discount",
              value: "-30%",
            },
          ],
        },
        {
          id: 4,
          frontImage: "4.webp",
          backImage: "4b.webp",
          brand: "Levi's",
          name: "Tee Unisex",
          price: 14.99,
          isInFavorites: false,
          badges: [
            {
              type: "tag",
              value: "Sostenibilità",
            },
            {
              type: "discount",
              value: "-50%",
            },
          ],
        },
        {
          id: 5,
          frontImage: "5.webp",
          backImage: "5b.webp",
          brand: "Maya Deluxe",
          name: "Stripe Bodice",
          price: 99.99,
          isInFavorites: true,
          badges: [
            {
              type: "tag",
              value: "Sostenibilità",
            },
            {
              type: "discount",
              value: "-50%",
            },
          ],
        },
        {
          id: 6,
          frontImage: "6.webp",
          backImage: "6b.webp",
          brand: "Esprit",
          name: "Maglione - Black",
          price: 29.99,
          isInFavorites: true,
          badges: [
            {
              type: "tag",
              value: "Sostenibilità",
            },
          ],
        },
      ],
    };
  },

};
</script>

<template>
  <main>
    <section>
      <div class="container">
        <div class="row">
          <!-- First Card -->
          <li class="column" v-for="(product, i) in products" :key="product.id" >
            <CardsComponent :item="product" />
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
