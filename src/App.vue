<template>
  <div id="app">
    <Header/>
    <Cards/>
    <Modal/>
    <Test/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Cards from './components/Cards.vue'
import Modal from './components/Modal.vue'
import Test from './components/Test.vue'

export default {
  name: 'app',
  components: {
    Header,
    Cards,
    Modal
  }
}

</script>
