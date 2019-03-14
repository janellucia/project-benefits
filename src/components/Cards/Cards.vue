<template>
  <b-container fluid>
    <b-row>
      <b-col cols="12" class="cards-wrapper">
        <div  class="sorting">
          <a href="#"><img alt="" src="../../assets/images/sort-icon.png"> Newest to Oldest</a>
        </div>
        <NotStarted/>
        <InProgress/>
        <Closed/>

        <div class="each-card not-started">
          <button v-b-modal.modalNotStarted class="settings" aria-label="settings"></button>
          <div class="card-header">
            <h3 class="project-name">Upgrade DRP</h3>
          </div>
          <div class="card-body">
            <p class="description">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
            <div>
              <h4>Project Benefits</h4>
              <p class="benefit">Makes internal processes more efficient/effective</p>
            </div>
          </div>
          <div class="card-footer">
            <p class="status">Closure Survey Not Started</p>
          </div>
          <div class="status-bar"></div>
        </div>

        <div class="each-card closed">
          <button class="settings"></button>
          <div class="card-header">
            <h3 class="project-name">Windows Upgrade</h3>
          </div>
          <div class="card-body">
            <p class="description">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
            <div>
              <h4>Project Benefits</h4>
              <p class="benefit">Makes internal processes more efficient/effective</p>
            </div>
          </div>
          <div class="card-footer">
            <p class="status">Closure Survey Closed</p>
          </div>
          <div class="status-bar"></div>
        </div>

        <button v-b-modal.modalAddProject class="add-project">
          <font-awesome-icon icon="plus-circle" />
          <h4>Add New Project</h4>
        </button>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>

import NotStarted from './NotStarted/NotStarted.vue'
import InProgress from './InProgress/InProgress.vue'
import Closed from './Closed/Closed.vue'

export default {
  name: 'Cards',
  components: {
    NotStarted,
    InProgress,
    Closed
  }
}
</script>


<style lang="scss" scoped>
@import './Cards.scss';
</style>
