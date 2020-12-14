<template>
  <div class="card_row md-layout md-gutter">
    <div class="md-layout-item ">
      <md-card class="cart_item orange" >
        <md-card-header >
          <md-avatar >
          <span class="img">
            <img :src="require('@/assets/svg/dman.svg')" alt="">
          </span>
          </md-avatar>
          <div class="md-title card_title">
            User Churn
          </div>
        </md-card-header>

        <md-card-content class="card_text">
          1907
        </md-card-content>

        <md-card-actions>
          <md-button>
     <span class="card_btn card_btn">
            Total
     </span>
          </md-button>
        </md-card-actions>
      </md-card>
    </div>
    <div class="md-layout-item">
      <md-card class="cart_item blue" >
        <md-card-header >
          <md-avatar >
          <span class="img">
            <img :src="require('@/assets/svg/lman.svg')" alt="">
          </span>
          </md-avatar>
          <div class="md-title card_title">
            User Churn
          </div>
        </md-card-header>

        <md-card-content class="card_text">
          0,5%
        </md-card-content>

        <md-card-actions>
          <md-button>
     <span class="card_btn card_btn">
           From 1.9%
     </span>
          </md-button>
        </md-card-actions>
      </md-card>
    </div>
    <div class="md-layout-item">
      <md-card class="cart_item gray" >
        <md-card-header >
          <md-avatar >
          <span class="img">
            <img :src="require('@/assets/svg/mun.svg')" alt="">
          </span>
          </md-avatar>
          <div class="md-title card_title">
            Nuw Customers
          </div>
        </md-card-header>

        <md-card-content class="card_text">
          48
        </md-card-content>

        <md-card-actions>
          <md-button>
     <span class="card_btn card_btn">
            From 56
     </span>
          </md-button>
        </md-card-actions>
      </md-card>
    </div>
  </div>
</template>
<style lang="scss" scoped>
@import "Card";
</style>
<script>
export default {
  name: 'Layouts',
  methods: {
    sendMessage () {
      window.alert('Send a message...')
    },
    doACall () {
      window.alert('Calling someone...')
    }
  }
}
</script>

