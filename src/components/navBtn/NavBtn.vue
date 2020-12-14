<template>
  <div class="header_btn">
    <md-button class="md-icon-button md-raised">
      <md-icon><img :src="require('@/assets/svg/bell.svg')" alt=""></md-icon>
    </md-button>

    <md-button class="md-icon-button md-raised md-primary">
      <md-icon><img :src="require('@/assets/svg/mail.svg')" alt=""></md-icon>
    </md-button>

    <md-button class="md-icon-button md-raised md-accent">
      <md-icon class="text">TL</md-icon>
    </md-button>
  </div>
</template>

<style lang="scss" scoped>
@import "NavBtn";
</style>

<script>
export default {
  name: 'NavBtn'
}
</script>