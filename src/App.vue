<template>
  <div id="app">
    <Header/>
    <Cards/>
    <Modal/>
    <PvNotStarted/>
    <PvInProgress/>
    <PvClosed/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Cards from './components/Cards.vue'
import Modal from './components/Modal.vue'
import PvNotStarted from './components/PvNotStarted.vue'
import PvInProgress from './components/PvInProgress.vue'
import PvClosed from './components/PvClosed.vue'

export default {
  name: 'app',
  components: {
    Header,
    Cards,
    Modal,
    PvNotStarted,
    PvInProgress,
    PvClosed
  }
}

</script>
