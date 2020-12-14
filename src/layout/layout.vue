<template>
  <div class="page-container">
    <md-app>
      <md-app-toolbar class="md-primary" md-elevation="0">
        <md-button class="md-icon-button" @click="toggleMenu" v-if="!menuVisible">
          <md-icon>
            <img :src="require('@/assets/svg/headerBTN.svg')" alt="">
          </md-icon>
        </md-button>
        <span class="md-title">
          <Select/>
        </span>
        <Navigation/>
        <NavBtn/>
      </md-app-toolbar>

      <md-app-drawer :md-active.sync="menuVisible" md-persistent="mini">
        <md-toolbar class="md-transparent" md-elevation="0">
          <span>Navigation</span>

          <div class="md-toolbar-section-end">
            <md-button class="md-icon-button md-dense" @click="toggleMenu">
              <md-icon>
                <img :src="require('@/assets/svg/star.svg')" alt="">
              </md-icon>
            </md-button>
          </div>
        </md-toolbar>

        <md-list>
          <md-list-item>
            <md-icon>
              <img :src="require('@/assets/svg/star.svg')" alt="">
            </md-icon>
            <span class="md-list-item-text">Inbox</span>
          </md-list-item>

          <md-list-item>
            <md-icon>
              <img :src="require('@/assets/svg/square.svg')" alt="">
            </md-icon>
            <span class="md-list-item-text">Sent Mail</span>
          </md-list-item>

          <md-list-item>
            <md-icon>
              <img :src="require('@/assets/svg/laitBell.svg')" alt="">
            </md-icon>
            <span class="md-list-item-text">Trash</span>
          </md-list-item>
        </md-list>
      </md-app-drawer>

      <md-app-content class="content" style="padding: 20px">

        <div class="md-layout md-gutter ">
          <div class="md-layout-item md-medium-size-100 md-xlarge-size-100 md-large-size-100">
            <Title/>
          </div>
          <div class="md-layout-item md-medium-size-66 md-xlarge-size-66 md-large-size-66">
            <div class="card">
              <Card/>
            </div>
          </div>

          <div class="md-layout-item md-medium-size-33 md-xlarge-size-33 md-large-size-33 ">
            <HorizontalBar/>
          </div>

          <div class="md-layout-item md-medium-size-66 md-xlarge-size-66 md-large-size-66 ">
            <Bar/>
          </div>

          <div class="md-layout-item md-medium-size-33 md-xlarge-size-33 md-large-size-33">
            <Histogram/>
          </div>

          <div class="md-layout-item md-medium-size-100 md-xlarge-size-100 md-large-size-100">
            <Table/>
          </div>
        </div>
      </md-app-content>
    </md-app>
  </div>
</template>

<style lang="scss" scoped>
@import "layout";
</style>

<script>
import Card from '@/components/card/Card'
import Table from '@/components/table/Table'
import Select from '@/components/select/Select'
import Navigation from '@/components/navigation/Navigation'
import Histogram from '@/components/histogram/Histogram'
import NavBtn from '@/components/navBtn/NavBtn'
import Bar from '@/components/bar/Bar'
import HorizontalBar from '@/components/horisontBar/HorisontBar'
import Title from '@/components/title/Title'


export default {
  name: 'Layout',
  components: {
    Title,
    HorizontalBar,
    NavBtn,
    Histogram,
    Table,
    Select,
    Navigation,
    Card,
    Bar

  },
  data: () => ({
    menuVisible: false
  }),
  methods: {
    toggleMenu() {
      this.menuVisible = !this.menuVisible
    }
  }
}
</script>


