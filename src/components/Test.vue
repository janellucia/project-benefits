<template>
  <div>
    <b-button v-b-modal.modalPreventTest>Launch demo modal</b-button>

    <!-- Main UI -->
    <div class="mt-3 mb-3">
      Submitted Names:
      <ul>
        <li v-for="n in names" v-bind:key="n.id">{{ n }}</li>
      </ul>
    </div>

    <!-- Modal Component -->
    <b-modal
      id="modalPreventTest"
      ref="modal"
      title="Submit your name"
      @ok="handleOk"
      @shown="clearName"
    >
      <form @submit.stop.prevent="handleSubmit">
        <b-form-input type="text" placeholder="Enter your name" v-model="name" />
      </form>
    </b-modal>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        name: '',
        names: []
      }
    },
    methods: {
      clearName() {
        this.name = ''
      },
      handleOk(evt) {
        // Prevent modal from closing
        evt.preventDefault()
        if (!this.name) {
          alert('Please enter your name')
        } else {
          this.handleSubmit()
        }
      },
      handleSubmit() {
        this.names.push(this.name)
        this.clearName()
        this.$nextTick(() => {
          // Wrapped in $nextTick to ensure DOM is rendered before closing
          this.$refs.modal.hide()
        })
      }
    }
  }
</script>
