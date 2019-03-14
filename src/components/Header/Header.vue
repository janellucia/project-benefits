<template>
  <div class="my-projects-header">
    <b-container>
      <b-row>
        <b-col md="6">
          <h2>My Project Dashboard</h2>
          <button class="add-project-button d-none d-md-block" v-b-modal.modalAddProject>Add Project</button>
        </b-col>
        <b-col md="6">
          <p>This Project Dashboard enables you to collect feedback to ensure your key projects are on track and to measure and communicate success.</p>
          <p>Manage your in-flight projects, track benefits realized and get reporting for both individual projects and at the portfolio level. <a href="#">Learn more</a></p>
          <button class="add-project-button d-block d-md-none" v-b-modal.modalAddProject>Add Project</button>
        </b-col>
    </b-row>
  </b-container>
  </div>
</template>

<script>

export default {
  name: 'Header'
}
</script>

<style lang="scss" scoped>
@import './Header.scss';
</style>
