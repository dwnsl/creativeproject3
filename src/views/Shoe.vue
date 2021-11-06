<template>
<div>
  <div class="info">
    <p>{{shoe.name}}</p>

    <p> Original Release Date: {{shoe.country}}</p>
    <p>Original Price: {{shoe.price}}</p>
  </div>
  <div class="image">
    <img :src="'/images/shoes/'+shoe.image">
  </div>
</div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      random: 0,
      amount: 0,
      shoe: {},
    }
  },
  created() {
    this.shoe = this.$root.$data.shoes.find(shoe=> shoe.id === parseInt(this.$route.params.id));
    this.random =
      Math.floor(Math.random() * 90) + 10;
    this.amount = this.random * parseFloat(this.shoe.price.replace(/\$|,/g, ''));
    this.amount = this.amount.toFixed(2);
  },
}
</script>

<style scoped>
.intro {
  font-style: italic;
}

.products {
  display: flex;
  flex-wrap: wrap;
}

.products img {
  border: 1px solid #333;
  height: 50px;
  width: 40px;
  margin-left: 10px;
  object-fit: cover;
}
</style>
