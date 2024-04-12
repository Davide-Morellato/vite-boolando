<script>
export default {
  //identifico la props per richiamare l'array nel MainSection
  props: {
    //creo un oggetto identificandolo
    item: {
      type: Object,
    },
  },
};
</script>

<template>
  <!-- card -->
  <div class="column">
    <div class="card">
      <div class="card-content">
        <img :src="`/img/${item.frontImage}`" :alt="`${item.name}`" />
        <ul>
          <li
            v-for="(badge, i) in item.badges"
            :key="i"
            :class="badge.type === 'discount' ? 'discount' : 'sustain'"
          >
            <span>{{ badge.value }}</span>
          </li>
          <!-- <li>
            <span class="sustain">Sostenibilità</span>
          </li> -->
          <li>
            <a href="#" class="b-heart">&hearts;</a>
          </li>
        </ul>
        <div class="card-hover">
          <img :src="`/img/${item.backImage}`" :alt="`${item.name}`" />
          <a href="#" class="r-heart">&hearts;</a>
        </div>
      </div>
      <div class="card-description">
        <ul>
          <li>
            <p class="brand">{{ item.brand }}</p>
          </li>
          <li>
            <h5 class="product">{{ item.name }}</h5>
          </li>
          <li v-for="(discount, i) in item.badges" :key="i">
            <div v-if="discount.value === '-50%' && discount.type === 'discount'">
                <span class="price">{{ (item.price - (item.price * 0.50)).toFixed(2) }} €</span>
                <span class="price-cout">{{ item.price }} €</span>
            </div>
            <div v-else-if="discount.value === '-30%' && discount.type === 'discount'">
                <span class="price">{{ (item.price - (item.price * 0.30)).toFixed(2) }} €</span>
                <span class="price-cout">{{ item.price }} €</span>
            </div>
            <div class="price" v-else-if="item.badges.length < 2 && discount.type === 'tag'">
                <span> {{ item.price }} € </span>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
