<template>

  <div :class="['project-view', {fullWidth: fullWidth}]">
    <div class="each-card not-started">
      <button v-b-toggle.notStarted @click="handleClick()">
        <span class="when-opened" aria-label="Close Settings">x</span> <span class="when-closed" aria-label="View Settings"></span>
      </button>
      <div class="card-body container">
        <h3 class="project-name">Application Upgrade <button class="trash float-right" aria-label="delete project"></button></h3>
        <input type="text" value="Application Upgrade" readonly>
        <div class="description-view">
          <p class="description">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
        </div>
        <div class="benefit-view">
          <h4 class="benefit-title">Project Benefits</h4>
          <h4 class="primary-title">Primary Benefit</h4>
          <p class="benefit">Makes internal processes more efficient/effective</p>
          <h4 class="secondary-title">Secondary Benefit</h4>
          <p class="benefit">Provides new internal capabilities</p>
        </div>
      </div>
      <div class="card-footer">
        <p class="status">Closure Survey Not Started</p>
      </div>
      <div class="status-bar"></div>
        <b-collapse id="notStarted">
          <b-container >
            <b-row class="pv-body">
              <div class="pv-status-bar"></div>
              <b-col md="12" class="results-header">
                <h4>Start Closure Survey</h4>
                <p>You’re almost there! Before you start, please take a moment to look over the survey questions at the bottom of the page. Then, decide if you would like to ask respondents about Project ROI or any custom questions.</p>
              </b-col>
              <button class="btn btn-launch">Launch Survey</button>
              <button class="btn btn-cancel">Cancel</button>
            </b-row>
            <b-row class="question-wrap">
              <b-col md="12">
                <button class="show-hide-questions">Hide Survey Questions</button>
              </b-col>
              <b-col md="12" visible id="surveyQuestions">
                <button class="btn btn-launch">Launch Survey</button>
                <button class="btn btn-cancel">Cancel</button>
              </b-col>
            </b-row>
        </b-container>
      </b-collapse>
    </div>
  </div>

</template>

<script>

export default {
  name: 'PvNotStarted',
  data() {
    return {fullWidth: false}
  },
  methods: {
    handleClick: function() {
      this.fullWidth = !this.fullWidth
    }
  }
}
</script>
