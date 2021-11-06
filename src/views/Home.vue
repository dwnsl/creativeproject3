<template>
<div>
  <p class="intro">Click on one of the shoes to learn about them</p>
  <p class="shoes">
    <router-link v-for="shoe in shoes" :key="shoe.id" :to="'/shoe/' + shoe.id">
       <img :src="'/images/shoes/'+shoe.image">
    </router-link>
  </p>
</div>
</template>

<script>
export default {
  name: 'Home',
  computed: {
    shoes() {
      return this.$root.$data.shoes;
    }
  }
}
</script>

<style scoped>
.intro {
  font-style: italic;
}

.shoes{
  display: flex;
  flex-wrap: wrap;
}

.shoes img {
  border: 1px solid #333;
  height: 300px;
  width: 500px;
  margin-left: 10px;
  object-fit: cover;
}
</style>
