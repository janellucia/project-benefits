<template>

  <div :class="['each-card', {fullWidth: fullWidth}]">
    <div class="not-started">
      <button v-b-toggle.notStarted @click="handleClick()">
        <span class="when-opened" aria-label="Close Settings">x</span> <span class="when-closed" aria-label="View Settings"></span>
      </button>
      <b-form>
        <div class="card-body container">

          <b-form-group id="projectNameGroup" label="Project Name" label-for="projectName">
            <h3 class="project-name"><b-form-input  id="projectName"  type="text" :placeholder="form.name" v-model="form.name" :disabled="disabled"/></h3>
            <button class="trash" aria-label="delete project" @click="handleEdit()"></button>
            <button class="save-button" @click="handleEdit()">Save</button>
            <button class="trash" aria-label="delete project"></button>
          </b-form-group>

          <div class="description-view">
            <b-form-group id="descriptionGroup" label="Description" label-for="description">
              <b-form-textarea id="description" class="description" type="text" rows="4" :placeholder="form.description" v-model="description" :disabled="disabled"/>
            </b-form-group>
          </div>

          <div class="benefit-view">
            <h4 class="benefit-title">Project Benefits</h4>
            <b-form-group id="primaryBenefitsGroup" label="Primary Project Benefit" label-for="primaryBenefits">
              <b-form-select id="primaryBenefits" :options="primaryOptions" v-model="primaryBenefit" :disabled="disabled"/>
            </b-form-group>
            <b-form-group id="secondaryBenefitsGroup" label="Secondary Project Benefit (Optional)" label-for="secondaryBenefits">
              <b-form-select id="secondaryBenefits" :options="secondaryOptions" v-model="secondaryBenefit" :disabled="disabled"/>
            </b-form-group>
          </div>
        </div>
      </b-form>
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
              <b-form class="col-md-12 cost-and-satisfaction-wrap">
                <b-row>
                  <b-col md="6">
                    <h5>Project Cost and ROI</h5>

                    <b-form-group id="projectCostGroup" label="Total Project Cost " label-for="projectCost">
                      <b-form-input id="projectCost" type="text" label="Project Name" v-model="cost" />
                    </b-form-group>

                    <p><span>Please estimate a total cost for this project.</span> This estimate does NOT need to be precise. If you are unsure of the cost, consider the following estimation process: (# of working days X # of working staff X $500) + Direct Project Costs.</p>

                    <b-form-group id="askEstimateGroup" description="Note: This will share your cost estimate with Project Sponsors." v-model="form.askEstimate">
                      <b-form-checkbox id="askEstimate" value="me">Ask Project Sponsors to estimate Project ROI (value relative to project cost)</b-form-checkbox>
                    </b-form-group>

                  </b-col>
                  <b-col md="6">
                    <h5>Custom Satisfaction Questions</h5>
                    <p>Please enter up to X custom satisfaction questions, which will be introduced with the following formatting:</p>

                    <b-form-group id="projectSatisfactionGroup" label="How satisfied are you with the following?" description="(User will choose: Very Satisfied, Somewhat Satisfied, Somewhat Dissatisfied, Very Dissatisfied)" label-for="projectSatisfaction">
                      <b-form-input id="projectSatisfaction" placeholder="Enter custom satisfaction factor, eg. creates new products or services" v-model="satisfaction" />
                    </b-form-group>

                    <a href="#" class="add-another-question">Add Question</a>

                  </b-col>
                </b-row>
                </b-form>
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
    return {
      fullWidth: false,
      disabled: true,
      displaySave: false,
      displayEdit: false,
      form: {
        name: 'Application Upgrade',
        description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
        primaryBenefit: null,
        secondaryBenefit: null,
        cost: '',
        askEstimate: [],
      },
      primaryOptions: [{ text: 'Makes internal processes more efficient/effective'}, 'Increases sales/revenue dollars', 'Makes internal processes more efficient/effective', 'Creates new products or services', 'Improves customer experience', 'Provides new internal capabilities', 'Reduces risk/Improves regulatory compliance', 'Improves quality of business management'],
      secondaryOptions: [{ text: 'Increases sales/revenue dollars'}, 'Increases sales/revenue dollars', 'Makes internal processes more efficient/effective', 'Creates new products or services', 'Improves customer experience', 'Provides new internal capabilities', 'Reduces risk/Improves regulatory compliance', 'Improves quality of business management'],
      show: true
    }
  },
  methods: {
    handleClick: function() {
      this.fullWidth = !this.fullWidth,
      this.disabled = !this.disabled
    },
    handleEdit: function() {
      this.displaySave = !this.displaySave
      this.displayEdit = !this.displayEdit
    }
  }
}
</script>
