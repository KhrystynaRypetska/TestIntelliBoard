<template>
  <div class="navigation_wrapper">
    <div class="navigation">
      <nav class="nav">
        <ul class="nav_list">
          <li
              class="nav_list_item"
              v-for="(nav, index) in navs.navigation"
              :key="index"
          >

           <router-link
           :to="nav.link">
             {{nav.name}}
           </router-link>

          </li>

        </ul>
      </nav>

    </div>
  </div>
</template>


<style lang="scss" scoped>
@import "Navigation.scss";
</style>
<script>
import header from '@/json/header.json'


export default  {
  name: 'Header',
  components: {

  },
  data(){
    return {
      navs: header
    }
  }
}
</script>