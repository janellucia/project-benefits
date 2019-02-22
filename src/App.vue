<template>
  <div id="app">
    <Header/>
    <Cards/>
     <modal v-if="showModal"> 
      <h3 slot="header" class="modal-title">
        Modal title
      </h3>
      <div slot="footer">
      <button type="button" class="btn btn-primary" data-dismiss="modal" @click="submitAndClose()">Add Project</button>
      <button type="button" class="btn btn-outline-info" @click="closeModal()">Cancel</button>
      </div>
    </modal>
    <button type="button" class="btn btn-primary" @click="openModal()">Open Modal</button>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Cards from './components/Cards.vue'
import Modal from './components/Modal.vue'

export default {
  name: 'app',
  components: {
    Header,
    Cards,
    Modal
  },
  data() {
    return {
      showModal: false
    }
  }, 
  methods: { 
    openModal() {
      this.showModal = true;
    },
    closeModal() {
      this.showModal = false;
    },
    submitAndClose() {
      this.showModal = false;
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
