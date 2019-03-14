<template>
  <div id="app">
    <Header/>
    <Cards/>
    <Modal/>
    <SurveyQuestions/>
  </div>
</template>

<script>
import Header from './components/Header/Header.vue'
import Cards from './components/Cards/Cards.vue'
import Modal from './components/Modal/Modal.vue'


export default {
  name: 'app',
  components: {
    Header,
    Cards,
    Modal,
  }
}

</script>
