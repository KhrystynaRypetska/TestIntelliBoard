<template>
  <Layout/>
<!--  <div id="app">-->
<!--    <div id="nav">-->
<!--      <router-link to="/">Home</router-link> |-->
<!--      <router-link to="/about">About</router-link>-->
<!--    </div>-->
<!--    <router-view/>-->
<!--  </div>-->
</template>

<style lang="scss">
@import "src/assets/scss/style.scss";
</style>

<script
    src="https://code.jquery.com/jquery-3.1.0.js"
    integrity="sha256-slogkvB1K3VOkzAI8QITxV3VzpOnkeNVsKvtkYLMjfk="
    crossorigin="anonymous">
</script>
<script>
import Layout from '@/layout/layout'
export  default {
  name: 'App',
  components: {
    Layout
  }
}
</script>
