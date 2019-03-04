<template>

  <div :class="['project-view', {fullWidth: fullWidth}]">
    <div class="each-card closed">
      <button v-b-toggle.closed @click="handleClick()">
        <span class="when-opened" aria-label="Close Settings">x</span> <span class="when-closed" aria-label="View Settings"></span>
      </button>
      <div class="card-body container">
        <h3 class="project-name">Security Upgrade <button class="trash float-right" aria-label="delete project"></button></h3>
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
        <p class="status">Closure Survey Closed</p>
      </div>
      <div class="status-bar"></div>
        <b-collapse id="closed">
          <b-container >
            <b-row class="pv-body">
              <div class="pv-status-bar"></div>
              <b-col md="12" class="results-header">
                <h4>Closure Survey Results</h4>
                <button class="trash float-right" aria-label="delete project"></button>
                <button class="close-survey-button float-right">Reopen Survey</button>
              </b-col>
              <b-col md="6" class="d-flex flex-column open-date-wrap">
                <p>Opened on</p>
                <h5>February 12, 2019</h5>
              </b-col>
            </b-row>
            <b-row class="stats">
              <b-col md="4" class="completion-stats">
                <h5>Completion Stats</h5>
                <div class="completed">
                  <p class="number">10</p>
                  <p class="type">Completed</p>
                </div>
                <div class="partial">
                  <p class="number">2</p>
                  <p class="type">Partial</p>
                </div>
                <h6>Overall</h6>
              </b-col>
              <b-col md="8" class="by-role">
                <h5>Survey Completions and Partial Responses by Role</h5>
                <div class="stats-breakdown d-flex">
                  <b-col>
                    <div class="completed">
                      <p class="number">2</p>
                      <p class="type">Completed</p>
                    </div>
                    <div class="partial">
                      <p class="number">1</p>
                      <p class="type">Partial</p>
                    </div>
                    <h6>Sponsor</h6>
                  </b-col>
                  <b-col>
                    <div class="completed">
                      <p class="number">8</p>
                      <p class="type">Completed</p>
                    </div>
                    <div class="partial">
                      <p class="number">0</p>
                      <p class="type">Partial</p>
                    </div>
                    <h6>Project Team</h6>
                  </b-col>
                  <b-col>
                    <div class="completed">
                      <p class="number">0</p>
                      <p class="type">Completed</p>
                    </div>
                    <div class="partial">
                      <p class="number">1</p>
                      <p class="type">Partial</p>
                    </div>
                    <h6>Impacted User</h6>
                  </b-col>
                </div>
              </b-col>
            </b-row>
            <button class="btn btn-download">Download Report</button>
            <button class="btn btn-book-call">Book an Analyst Call</button>
        </b-container>
      </b-collapse>
    </div>
  </div>

</template>

<script>

export default {
  name: 'PvClosed',
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
