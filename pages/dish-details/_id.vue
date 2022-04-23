<template>
<body class="flex items-stretch bg-white">
<div class="container">
    <div class="content-container">
        <div><h1 class="my-8 text-sky">{{dish.title}}</h1></div>
        <span class="pr-3 border-r-2 text-sm">{{dish.author}}</span>
        <span class="pr-3 pl-2 border-r-2 text-sm">{{dish.date}}</span>
        <span class="pl-2 text-sm">{{dish.category}}</span>
        <div class="flex justify-center"><img class="mb-8" :src="dish.image" /></div>
        <div><p class="mb-8">{{dish.description}}</p></div>
        <div class="text-content z-0"><nuxt-content :document="dish" class="mb-32"></nuxt-content></div>
    </div>
</div>
</body>
</template>
<script>
import "C:/Development/nuxt/nuxt-Blog/assets/css/css.css";

export default {
    async asyncData({$content, params}) {
        
        let dish = await $content('dishes/dish'+params.id).fetch()
        console.log(dish)

        return {
            dish
        }
    },
}
</script>

<style>

</style>