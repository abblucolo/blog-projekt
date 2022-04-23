<template>
    <div class="bg-white">
        <div><img :src="item.image" alt="dish image" class="h-80 w-120 object-cover mb-2"></div>
        <span class="pr-3 border-r-2 text-sm">{{item.date}}</span>
        <span class="pl-2 text-sm">{{item.author}}</span>
        <div><h2>{{item.title}}</h2></div>
        <div><p>{{item.description}}</p></div>
    </div>
</template>

<script>
import "../assets/css/css.css";

export default {
    props:['item'],
    data() {
        return {

        }
    }
}
</script>