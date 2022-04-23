<template>
<div>
    <!--<HeaderComponent></HeaderComponent>-->
    <NavBar></NavBar>
  <div class="bg-sky">
    <ul class="text-white container">
      <li id="changeColour" class="inline-block p-2"><a href="/">Blog</a></li>
      <li id="changeColour" class="inline-block p-2"><a href="/about">About</a></li>
      <li id="changeColour" class="inline-block p-2"><a href="/contact">Contact</a></li>
    </ul>
  </div>
    <nuxt/>
    <FooterComponent></FooterComponent>
</div>
</template>

<script>
import "../assets/css/css.css";

export default {
}
</script>

<style>
#changeColour:hover {
    background-color: #ff671f;
}
</style>