<template>
  <div>

    <!-- Main UI -->
    <div class="each-card not-started">
      <button class="settings"></button>
      <div class="card-header">
        <h3 v-for="n in names" v-bind:key="n.id" class="project-name">{{ n }}</h3>
      </div>
      <div class="card-body">
        <p class="description" v-for="d in descriptions" v-bind:key="d.id" >{{ d }}</p>
        <div>
          <h4>Project Benefits</h4>
          <p class="benefit" v-for="p in primaryBenefits" v-bind:key="p.id" >{{ p }}</p>
          <p class="benefit" v-for="s in secondaryBenefits" v-bind:key="s.id" >{{ s }}</p>
        </div>
      </div>
      <div class="card-footer">
        <p class="status">Closure Survey Not Started</p>
      </div>
      <div class="status-bar"></div>
    </div>

    <!-- Modal Component -->
    <b-modal id="modalAddProject" ref="modal" title="Add New Project" ok-title="Add Project" ok-variant="add-project" cancel-variant="cancel" @ok="handleOk" @shown="clearName" >
      <form @submit.stop.prevent="handleSubmit">

        <b-form-group id="projectNameGroup" label="Project Name" label-for="projectName">
          <b-form-input id="projectName" type="text" label="Project Name" v-model="name" />
        </b-form-group>

        <b-form-group id="descriptionGroup" label="Description" label-for="exampleInput2">
          <b-form-textarea type="text" v-model="description" />
        </b-form-group>

        <b-form-group id="primaryBenefitsGroup" label="Primary Project Benefit" label-for="primaryBenefits">
          <b-form-select id="primaryBenefits" :options="options" v-model="primaryBenefit" />
        </b-form-group>

        <b-form-group id="secondaryBenefitsGroup" label="Secondary Project Benefit" label-for="secondaryBenefits">
          <b-form-select id="secondaryBenefits" :options="options" v-model="secondaryBenefit" />
        </b-form-group>

      </form>
    </b-modal>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        name: ' ',
        names: [],
        description: ' ',
        descriptions: [],
        primaryBenefit: '',
        primaryBenefits: [],
        secondaryBenefit: '',
        secondaryBenefits: [],
        options: [{ text: 'Select Benefit', value: null }, 'Increases sales/revenue dollars', 'Makes internal processes more efficient/effective', 'Creates new products or services', 'Improves customer experience', 'Provides new internal capabilities', 'Reduces risk/Improves regulatory compliance', 'Improves quality of business management'],
      }
    },
    methods: {
      clearName() {
        this.name = '',
        this.description = '',
        this.primaryBenefit = '',
        this.secondaryBenefit = ''
      },
      handleOk(evt) {
        // Prevent modal from closing
        evt.preventDefault()
        if (!this.name) {
          alert('Please enter your name')
        } else if (!this.description) {
          alert('Please enter a description')
        } else if (!this.primaryBenefit) {
          alert('Please select a PrimaryBenefit')
        }else {
          this.handleSubmit()
        }
      },
      handleSubmit() {
        this.names.push(this.name)
        this.descriptions.push(this.description)
        this.primaryBenefits.push(this.primaryBenefit)
        this.secondaryBenefits.push(this.secondaryBenefit)
        this.clearName()
        this.$nextTick(() => {
          // Wrapped in $nextTick to ensure DOM is rendered before closing
          this.$refs.modal.hide()
        })
      }
    }
  }
</script>
