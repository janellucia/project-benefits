<template>
  <div>
    <button v-b-modal.modalPrevent>test modal</button>

    <!-- Main UI -->
    <div class="mt-3 mb-3">
      Submitted Names:
      <ul>
        <li v-for="n in names" v-bind:key="n.id">{{ n }}</li>
      </ul>
      <div>
        <p v-for="p in projectNames" v-bind:key="p.id">{{ p }}</p>
      </div>
    </div>

    <!-- Modal Component -->
    <b-modal
      id="modalPrevent"
      ref="modal"
      title="Add New Project"
      ok-title="Add Project"
      ok-variant="add-project"
      cancel-variant="cancel"
      @ok="handleOk"
      @shown="clearName"
    >
      <form @submit.stop.prevent="handleSubmit">

        <b-form-group id="projectNameGroup" label="Project Name" label-for="projectName" v-modal="projectName">
          <b-form-input
            id="projectName"
            type="text"
            required />
        </b-form-group>

        <b-form-group id="descriptionGroup" label="Description" label-for="exampleInput2">
          <b-form-textarea
            id="description"
            type="text"
            required />
        </b-form-group>

        <b-form-group id="primaryBenefitsGroup" label="Primary Project Benefit" label-for="primaryBenefits">
          <b-form-select id="primaryBenefits" :options="primaryBenefits" required v-model="form.primaryBenefit" />
        </b-form-group>

        <b-form-group id="secondaryBenefitsGroup" label="Secondary Project Benefit" label-for="secondaryBenefits">
          <b-form-select id="secondaryBenefits" :options="secondaryBenefits" required v-model="form.secondaryBenefit" />
        </b-form-group>

      </form>
    </b-modal>
  </div>
</template>

<script>

export default {
  data() {
      return {
        name: '',
        names: [],
        projectName: '',
        projectNames: [],
        form: {
          pojectName: '',
          description: '',
          primaryBenefit: null,
          secondaryBenefit: null,
        },
        primaryBenefits: [{ text: 'Select Benefit', value: null }, 'Increases sales/revenue dollars', 'Makes internal processes more efficient/effective', 'Creates new products or services', 'Improves customer experience', 'Provides new internal capabilities', 'Reduces risk/Improves regulatory compliance', 'Improves quality of business management'],
        secondaryBenefits: [{ text: 'Select Benefit', value: null }, 'Increases sales/revenue dollars', 'Makes internal processes more efficient/effective', 'Creates new products or services', 'Improves customer experience', 'Provides new internal capabilities', 'Reduces risk/Improves regulatory compliance', 'Improves quality of business management'],
        show: true
      }
    },
    methods: {
      clearName() {
        this.projectName = ''
      },
      handleOk(evt) {
        // Prevent modal from closing
        evt.preventDefault()
        if (!this.projectName) {
          alert('Please enter your Project Name')
        } else {
          this.handleSubmit()
        }
      },
      handleSubmit() {
        this.projectNames.push(this.projectName)
        this.clearName()
        this.$nextTick(() => {
          // Wrapped in $nextTick to ensure DOM is rendered before closing
          this.$refs.modal.hide()
        })
      }
    }
  }

</script>
