<template>
  <div class="container-fluid">
    <div class="row">
      <div class="cards-wrapper col-md-12">
        <div  class="sorting">
          <a href="#"><img alt="" src="../assets/images/sort-icon.png"> Newest to Oldest</a>
        </div>

        <div class="each-card not-started">
          <font-awesome-icon icon="cog" />
          <div class="card-header">
            <h3 class="project-name">Application Upgrade</h3>
          </div>
          <div class="card-body">
            <p class="description">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
            <div>
              <h4>Project Benefits</h4>
              <p class="benefit">Makes internal processes more efficient/effective</p>
            </div>
          </div>
          <div class="card-footer">
            <p class="status">Closure Survey Not Started</p>
          </div>
          <div class="status-bar"></div>
        </div>

        <div class="each-card in-progress">
          <font-awesome-icon icon="cog" />
          <div class="card-header">
            <h3 class="project-name">Risk Analysis</h3>
          </div>
          <div class="card-body">
            <p class="description">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
            <div>
              <h4>Project Benefits</h4>
              <p class="benefit">Makes internal processes more efficient/effective</p>
            </div>
          </div>
          <div class="card-footer">
            <p class="status">Closure Survey In Progress</p>
          </div>
          <div class="status-bar"></div>
        </div>

        <div class="each-card closed">
          <font-awesome-icon icon="cog" />
          <div class="card-header">
            <h3 class="project-name">Security Upgrade</h3>
          </div>
          <div class="card-body">
            <p class="description">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
            <div>
              <h4>Project Benefits</h4>
              <p class="benefit">Makes internal processes more efficient/effective</p>
            </div>
          </div>
          <div class="card-footer">
            <p class="status">Closure Survey Closed</p>
          </div>
          <div class="status-bar"></div>
        </div>

        <div class="each-card not-started">
          <font-awesome-icon icon="cog" />
          <div class="card-header">
            <h3 class="project-name">Upgrade DRP</h3>
          </div>
          <div class="card-body">
            <p class="description">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
            <div>
              <h4>Project Benefits</h4>
              <p class="benefit">Makes internal processes more efficient/effective</p>
            </div>
          </div>
          <div class="card-footer">
            <p class="status">Closure Survey Not Started</p>
          </div>
          <div class="status-bar"></div>
        </div>

        <div class="each-card closed">
          <font-awesome-icon icon="cog" />
          <div class="card-header">
            <h3 class="project-name">Windows Upgrade</h3>
          </div>
          <div class="card-body">
            <p class="description">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
            <div>
              <h4>Project Benefits</h4>
              <p class="benefit">Makes internal processes more efficient/effective</p>
            </div>
          </div>
          <div class="card-footer">
            <p class="status">Closure Survey Closed</p>
          </div>
          <div class="status-bar"></div>
        </div>

        <a href="#" class="add-project">
          <font-awesome-icon icon="plus-circle" />
          <h4>Add New Project</h4>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Cards',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
