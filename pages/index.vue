<template>
<body class="bg-blue-100">
  <div class="container">
    <div class="content-container">
      <div @click="goToDish(dish.id)" class="m-4 p-5 bg-white" v-for="dish in dishes" :key="dish.id">
      <DishListItem :item="dish"></DishListItem>
      </div>
    </div>
  </div>
</body>
</template>

<script>
import "../assets/css/css.css";

export default {
  name: 'IndexPage',
    async asyncData({$content}) {
    let dishes = await $content('dishes').without(['body']).fetch()

    return {
      dishes
    }
  },
  methods: {
    goToDish(id) {
      this.$router.push('/dish-details/'+id)
    }
  }
}
</script>