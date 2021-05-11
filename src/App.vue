<template>
  <div id="app">
    <div id="nav">
    <div>
      <b-navbar toggleable="lg" type="light" variant="light" class="ml-auto fixed-top">

          <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

          <div class="d-flex bd-highlight ">
              <h5
                class="font-weight-bolder"
                style="
                  margin-left: 10px;
                  margin-top: 18px;
                  font-family: 'Poppins', sans-serif;
                  color: Teal;
                "
              >
                Cityscapes
              </h5>
          </div>

              <b-collapse id="nav-collapse" is-nav>
                <b-navbar-nav class="ml-auto">
                  <b-nav-item class="let"> <router-link to="/">Home</router-link> </b-nav-item>
                    <b-nav-item class="let"> <router-link to="/about">About Us</router-link></b-nav-item>
                  <b-nav-item class="let"> <router-link to="/Services">Services</router-link></b-nav-item>
                  <b-nav-item class="let"> <router-link to="/Projects">Projects</router-link></b-nav-item>
                  <b-nav-item class="let"> <router-link to="/Contact">Contact Us</router-link> </b-nav-item>
                  </b-navbar-nav>
                  </b-collapse>
                </b-navbar>
        </div>
      </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: rgb(142, 182, 114);
    }
  }
}

.let {
  padding-top: 14px 30px;
  margin-right: 30px;
  font-size: 17px;
}
</style>
