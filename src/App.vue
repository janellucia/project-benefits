<template>
  <div id="app">
    <Header/>
    <Cards/>
    <Modal/>
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
  }
}

</script>
