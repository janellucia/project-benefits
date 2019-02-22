<template>
  <div class="my-projects-header">
    <modal v-if="showModal"> 
      <h4 slot="header" class="modal-title">
        Add New Project
      </h4>
      <div slot="footer">
        <button type="button" class="btn btn-primary" data-dismiss="modal" @click="submitAndClose()">Add Project</button>
        <button type="button" class="btn btn-outline-info" @click="closeModal()">Cancel</button>
      </div>
    </modal>
    <b-container>
      <b-row>
        <b-col cols="6">
          <h2>My Project Dashboard</h2>
          <button class="add-project-button" @click="openModal()">Add Project</button>
        </b-col>
        <b-col cols="6">
          <p>This Project Dashboard enables you to collect feedback to ensure your key projects are on track and to measure and communicate success.</p>
          <p>Manage your in-flight projects, track benefits realized and get reporting for both individual projects and at the portfolio level. <a href="#">Learn more</a></p>
        </b-col>
    </b-row>
  </b-container>
  </div>
</template>

<script>

import Modal from './Modal.vue'

export default {
  name: 'Header',
  components: {
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
