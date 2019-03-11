<template>
  <div id="app">
    <Header/>
    <Cards/>
    <Modal/>
    <SurveyQuestions/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Cards from './components/Cards.vue'
import Modal from './components/Modal.vue'
import SurveyQuestions from './components/SurveyQuestions.vue'


export default {
  name: 'app',
  components: {
    Header,
    Cards,
    Modal,
    SurveyQuestions
  }
}

</script>
