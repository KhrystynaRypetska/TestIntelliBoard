<template>
  <div class="select md-layout md-gutter">
    <div class="select_wrapper md-layout-item">
      <div class="select_img">
        <img :src="require('@/assets/svg/twiter.svg')" alt="">
      </div>
      <md-field>

        <md-select v-model="selectedMovies" name="movies" id="movies" multiple>
          <md-option class="select_option" value="fight-club">Fight Club</md-option>
          <md-option class="select_option" value="godfather">Godfather</md-option>
          <md-option class="select_option" value="godfather-ii">Godfather II</md-option>
          <md-option class="select_option" value="godfather-iii">Godfather III</md-option>
          <md-option class="select_option" value="godfellas">Godfellas</md-option>
          <md-option class="select_option" value="pulp-fiction">Pulp Fiction</md-option>
          <md-option value="scarface">Scarface</md-option>
        </md-select>
        <label class="select_title"  for="movies">IB Demo Connection</label>
      </md-field>
      <div class="select_img-btn">
        <img :src="require('@/assets/svg/vector.svg')" alt="">
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "Select.scss";
</style>
<script>
export default {
  name: 'MultipleSelect',
  data: () => ({
    selectedMovies: [

    ]
  })
}
</script>
